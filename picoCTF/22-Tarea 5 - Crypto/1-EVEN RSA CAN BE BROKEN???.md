## EVEN RSA CAN BE BROKEN???

### Descripción
This service provides you an encrypted flag. Can you decrypt it with just N & e?
### Solución

#### Solución 1
```
N = 26564042648354246651130498601747265107607538880932807514165006472314180656964302548663573229480453304284738345663739925494861393694636317160602264960551482
e = 65537
c = 20075940260748291009829773838488741566487784607969581469191315448823899407032602600797153319611441297433097126041894565824941705698344081167831491247957277

# factor N (it's even)
p = N // 2
phi = p - 1

# modular inverse (extended Euclidean algorithm)
def egcd(a, b):
    if a == 0:
        return b, 0, 1
    g, y, x = egcd(b % a, a)
    return g, x - (b // a) * y, y

def modinv(a, m):
    g, x, _ = egcd(a, m)
    if g != 1:
        raise Exception('modular inverse does not exist')
    return x % m

d = modinv(e, phi)

# decrypt
m = pow(c, d, N)

# convert int to bytes
def int_to_bytes(x):
    return x.to_bytes((x.bit_length() + 7) // 8, 'big')

print(int_to_bytes(m).decode())
```

picoCTF{tw0_1$_pr!m3de643ad5}

### Notas adicionales


### Referencias

-