```
TYPES:
 BEGIN OF ty_s_data,

 vbeln TYPE vbap-vbeln,
 netwr TYPE vbap-netwr,
 t_color TYPE lvc_t_scol, "Color column
 END OF ty_s_data.

DATA mt_data TYPE TABLE OF ty_s_data.

SELECT vbeln netwr FROM vbap INTO corresponding fields of TABLE mt_data up to 10 rows.

LOOP AT mt_data ASSIGNING FIELD-SYMBOL(<s_data>).
  IF <s_data>-netwr > 5000.
    APPEND VALUE #( color-col = col_negative color-int = 0 color-inv = 0 ) TO <s_data>-t_color.
  ENDIF.
ENDLOOP.


DATA: lo_alv TYPE REF TO cl_salv_table.

    cl_salv_table=>factory(
      IMPORTING
        r_salv_table = lo_alv
      CHANGING
        t_table      = mt_data )
    .

lo_alv->get_functions( )->set_all( abap_true ).
lo_alv->get_columns( )->set_optimize( abap_true ).
lo_alv->get_columns( )->set_color_column( 'T_COLOR' ).
lo_alv->display( ).
*#END
```
