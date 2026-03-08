## MatchTheRegex

### Descripción
How about trying to match a regular expression

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
El código fuente nos dice:
```
<script>
	function send_request() {
		let val = document.getElementById("name").value;
		// ^p.....F!?
		fetch(`/flag?input=${val}`)
			.then(res => res.text())
			.then(res => {
				const res_json = JSON.parse(res);
				alert(res_json.flag)
				return false;
			})
		return false;
	}

</script>
```
// ^p.....F!?
p y luego 5 caracteres y después F, y después puede haber cualquier caracter.

Introducimos: p12345F

Obtenemos:

picoCTF{succ3ssfully_matchtheregex_2375af79}
### Notas adicionales
Las expresiones regulares (regex o regexp) son secuencias de caracteres que forman un patrón de búsqueda, utilizadas para buscar, editar, manipular y validar texto. Actúan como comodines avanzados que permiten encontrar combinaciones específicas de caracteres dentro de cadenas de texto. Se utilizan en programación para validar datos (como emails), buscar archivos y reemplazar texto. 

### Referencias

-