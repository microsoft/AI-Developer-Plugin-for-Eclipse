
## Writing Data from a table to a file
<b> Provide following in the comment. Either you can sorround these comments in #START and #END or select these lines to pass multiple lines to AIDT plugin code generation function.</b>
Define a selection field to take customer number  and file path as input
Provide field names with table to declare a structure
Declare a type with fields and internal table
customer    name  street    city
kunnr  name1  stras ort01 regio
from KNA1
select data from KNA1 to this internal table
loop in the internal table write the data comma separated to the file given in the input

