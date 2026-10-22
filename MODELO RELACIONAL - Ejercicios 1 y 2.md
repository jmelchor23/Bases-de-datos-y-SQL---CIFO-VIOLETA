**MODELO RELACIONAL**



**EJERCICIO 1. Artículos y encargos** 







PEDIDO **num\_pedido,** fecha\_hora\_ped, dir\_envio, id\_cliente, id\_direccion

&#x09;donde:

&#x09;id\_cliente REFERENCIA CLIENTES

&#x09;id\_direccion referencia DIRECCION\_ENVIO



CLIENTES **id\_cliente**, saldo, limite\_de\_credito, descuento, id\_direccion

&#x09;donde:

&#x09;id\_direccion referencia DIRECCION\_ENVIO



DIRECCION\_ENVIO **id\_direccion**, calle, numero, ciudad, cp 



DIRECCION\_CLIENTE **(id\_cliente + id\_direccion)**

&#x09;donde:

&#x09;id\_cliente referencia CLIENTES

&#x09;id\_direccion referencia DIRECCION\_ENVIO



DETALLES PEDIDO **num\_articulo**, cantidad, num\_pedido

&#x09;donde:

&#x09;num\_pedido referencia PEDIDO



ARTICULO **id\_articulo**, fabricas\_dist, exitencias, descripcion\_art



ARTICULOS\_PEDIDO  (**num\_articulo + id\_articulo**)

&#x09;donde

&#x09;num\_articulo referencia DETALLES PEDIDO

&#x09;id\_articulo referencia ARTICULO



FABRICA **id\_fabrica**, telefono, total\_articulos, fabricas\_alternativas



ARTUCULOS\_X\_FABRICA (**id\_articulo + id\_fabrica**)

&#x09;donde:

&#x09;id\_fabrica referencia FABRICA

&#x09;id\_artuclo referencia ARTICULO



\-----------------------------------------------------------------------------



**EJERCICIO 2. Sistema de ventas**







PROVEEDOR **Cif/Nif,**  Nombre, Telefono, P\_web, Calle, Numero, Ciudad, CP, Id\_producto



PRODUCTO **Id\_producto,** Nombre, Precio\_actual, Stock, proveedor,Id\_categoria, nombre\_cat, descripcion



PROVEEDOR\_PRODUCTO (**Cif/Nif + Id\_producto**)

donde:	

&#x09;**Cif/Nif** referencia PROVEEDOR

&#x09;**Id\_producto** referencia PRODUCTO



FACTURA **Num\_factura,** Cliente, Fecha, Descuento, Importe\_iva





PRODUCTO\_FACTURA (**Id\_producto + num\_factura,** precio\_producto, cantidad, Importe)

donde:

&#x09;**Id\_producto** referencia PRODUCTO

&#x09;**num\_factura** referencia FACTURA



CLIENTE **Cif/Nif,** Nombre, calle, numero, ciudad, cp

TELEFONOS\_CLIENTE **id\_cliente**, telefono\_1, telefono\_2, Cif/Nif

donde:

&#x09;Cif/Nif referencia CLIENTE

&#x09;



















