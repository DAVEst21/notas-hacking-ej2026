## MacroHard WeakEdge

### Descripción
I've hidden a flag in this file. Can you find it?[Forensics_is_fun.pptm](https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm)
### Solución

#### Solución 1
Abrimos el archivo `Forensics is fun.pptm` con `binwalk` para analizar su contenido interno:

```
binwalk 'Forensics is fun.pptm'
```

Notaremos que el archivo es un contenedor ZIP que contiene múltiples archivos y carpetas. En la salida de `binwalk`, veremos una entrada llamada `ppt/slideMasters/hidden` que resulta sospechosa.

Extraemos todos los archivos con:

```
binwalk -e 'Forensics is fun.pptm'
```

Esto creará una carpeta llamada `_Forensics is fun.pptm.extracted`. Dentro de ella, navegamos hasta la ruta donde está el archivo oculto:

```
cd _Forensics\ is\ fun.pptm.extracted/ppt/slideMasters/
```

Listamos el contenido con `ls` y veremos el archivo `hidden`. Lo leemos con:

```
cat hidden
```

Obtendremos una cadena de letras separadas por espacios: `Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q`.

Notaremos que esta cadena parece estar codificada en Base64. Primero eliminamos los espacios:

```
cat hidden | tr -d ' '
```

Esto nos dará: `ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ`.

Decodificamos con Base64:

```
cat hidden | tr -d ' ' | base64 -d
```

Obtenemos la flag: `picoCTF{D1d_u_kn0w_ppts_r_z1p5}`
### Notas adicionales

### Referencias

-