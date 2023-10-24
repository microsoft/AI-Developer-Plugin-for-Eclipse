TYPES: BEGIN OF ty_customer,
            customer_id TYPE kna1-kunnr,
            name1 TYPE kna1-name1,
            city TYPE kna1-city1,
       END OF ty_customer.

DATA: it_customers TYPE TABLE OF ty_customer,
      wa_customer TYPE ty_customer,
      wa_sales TYPE bapivbap.

*--Populate the internal table with data
SELECT kunnr name1 city1 FROM kna1 INTO TABLE it_customers.

LOOP AT it_customers INTO wa_customer.
  CLEAR wa_sales.
  SELECT SINGLE vbeln FROM vbak
         WHERE kunnr = wa_customer-customer_id
              AND vbtyp = 'C'
         INTO wa_sales-vbeln.
  wa_customer-sales_order = wa_sales-vbeln.
ENDLOOP.

*--Create an instance of the ALV
DATA: alv_grid TYPE REF TO cl_gui_alv_grid.

CREATE OBJECT alv_grid
  EXPORTING i_parent = cl_gui_container=>screen0.

*--Set the properties of the ALV
CALL METHOD alv_grid->set_table_for_first_display
  EXPORTING
    i_structure_name = 'TY_CUSTOMER'
  CHANGING
    it_outtab = it_customers.

CALL METHOD alv_grid->set_layout
  EXPORTING
    is_layout = t_layout.

CALL METHOD alv_grid->set_sort_info
  EXPORTING
    is_sortinfo_fieldname = 'CUSTOMER_ID'.

*--Display the ALV
CALL METHOD alv_grid->display.
