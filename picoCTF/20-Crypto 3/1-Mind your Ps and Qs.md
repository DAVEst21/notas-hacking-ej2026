## Mind your Ps and Qs

### Descripción
In RSA, a small e value can be problematic, but what about N? Can you decrypt this? [values](https://challenge-files.picoctf.net/c_wily_courier/f5f0388785f1835df56b6c50fcbe25d88004d2c3184fe7191b852514bf04941a/values)
### Solución

#### Solución 1
```
c = 15341890103764929939105506004034128738090325640037083301857608662849501626260517

n = 948406957756830799684818171639547165784816468744946013083947881743680617123566349

e = 65537

  

# se obtienen de la factorizacion en factordb.com

p = 1891771437429478964908181306574287207137

q = 501332739776173570344039681219489434626477

  

tn = (p-1) * (q-1)

d = pow(e, -1, tn)

m = pow(c,d,n)

  

hex_str = hex(m)[2:]

  

# verifica que los digitos hexadecimales sean un numero par

if len(hex_str) % 2 != 0:

hex_str = '0' + hex_str

  

decoded = bytes.fromhex(hex_str).decode()

print(f'\nDecodificado: {decoded}')

  

flag = decoded[::-1]

print(f'\nFlag : {flag}')
```

```
Decodificado: 
}19ea7cd1_do0g_0n_N_11ams{FTCocip

Flag : picoCTF{sma11_N_n0_g0od_1dc7ae91}
```

### Notas adicionales
### Referencias

-