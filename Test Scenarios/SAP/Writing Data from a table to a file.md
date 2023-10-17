
## Writing Data from a table to a file
<b> Provide following in the comment. Either you can sorround these comments in #START and #END or select these lines to pass multiple lines to AIDT plugin code generation function.</b>
<code>
*#START
*Define select options to take multiple customer number   and a parameter to take local file path as input
*Provide field names with table to declare a structure
*Declare a type with fields and internal table
*customer    name  street    city
*kunnr  name1  stras ort01 regio
*from KNA1
*select data from KNA1 to this internal table
*looping in the internal table generate comma separated text and populate in an internal table
*download table to the file given in the input
*#END
</code>

Test this further by adding a new comment before download table code to write data in json format. select all lines with the below code to test this function
<code>*Rewrite above code to concatenate fields from it_customer in json format.</code>
Remove any command like text from the editor to make it more accurate
