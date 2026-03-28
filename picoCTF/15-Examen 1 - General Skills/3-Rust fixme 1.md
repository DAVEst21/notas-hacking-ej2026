## Descripción 
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
## Solución 

Descargamos y descomprimimos el archivo
```
$ tar -xzvf fixme1.tar.gz 
```
Entramos a carpeta fixme1/src y editamos el documento main.rs, se trata de corregir el código como se muestra a continuación (seguir indicaciones de los comentarios):
```
use xor_cryptor::XORCryptor;

fn main() {
    // Key for decryption
    let key = String::from("CSUCKS"); // How do we end statements in Rust?

    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", ">

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    // Create decrpytion object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return; // How do we return in rust?
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    println!("{}", String::from_utf8_lossy(&decrypted_buffer));

}
```

Primero, instala Rust (si aún no lo tienes instalado). Puedes encontrar más información aquí.

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Crea un nuevo proyecto para el código.

```
cargo new rust_fixme1
```

Compila y ejecuta el programa

```
cargo run
```

picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}
## Notas
## Referencias