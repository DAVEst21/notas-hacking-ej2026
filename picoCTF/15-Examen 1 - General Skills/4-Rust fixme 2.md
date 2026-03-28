## Descripción 
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).

## Solución 
Igual que al anterior, se descomprime y se corrige lo indicado en comentarios de este código main.rs en fixme2/src
```
use xor_cryptor::XORCryptor;

// FIX: Changed the function parameter to accept a mutable reference (&mut String)
// so that the function can modify the passed string.
fn decrypt(encrypted_buffer: Vec<u8>, borrowed_string: &mut String) {
    // Key for decryption
    // FIX: Added a semicolon at the end of the statement.
    let key = String::from("CSUCKS");

    // Editing our borrowed value
    borrowed_string.push_str("PARTY FOUL! Here is your flag: ");

    // Create decryption object
    let res = XORCryptor::new(&key);
    // FIX: Correctly returning early from the function using `return;` when an error occurs.
    if res.is_err() {
        return;
    }
    let xrc = res.unwrap();

    // Decrypt flag and append it to the borrowed_string
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    borrowed_string.push_str(&String::from_utf8_lossy(&decrypted_buffer));
    
    // FIX: Corrected the println! syntax to properly output the variable.
    println!("{}", borrowed_string);
}

fn main() {
    // Encrypted flag values
    let hex_values = [
        "41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61",
        "25", "0d", "c4", "60", "f2", "12", "a0", "18", "03", "51", "03", "36", "05", "0e", "f9",
        "42", "5b",
    ];

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values
        .iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    // FIX: Declared the variable as mutable using 'mut' since we need to modify it.
    let mut party_foul = String::from("Using memory unsafe languages is a: ");
    
    // FIX: Passed a mutable reference (&mut party_foul) to allow the function to modify the original string.
    decrypt(encrypted_buffer, &mut party_foul);
}

```
Crea un nuevo proyecto para el código.

```
cargo new rust_fixme2
```

Compila y ejecuta el programa

```
cargo run
```

picoCTF{4r3_y0u_h4v1n5_fun_y31?}

## Notas
## Referencias