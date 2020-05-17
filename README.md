## Crear base de datos

Cliente mysql
```
docker run -it --network wordpress --rm mysql:5.7 mysql -hdb -uroot -padmin
```

Antes de instalar el wordpress:
```
CREATE DATABASE <nombre_bd> CHARACTER SET utf8 COLLATE utf8_general_ci;
GRANT ALL PRIVILEGES ON <nombre_bd>.* TO "<user_name>"@"%" IDENTIFIED BY "<user_pass>";
```

Comprobar permisos:
```
mysql> SHOW GRANTS FOR 'wordpress';
+----------------------------------------------------------+
| GRANTS FOR wordpress@%                                   |
+----------------------------------------------------------+
| GRANT USAGE ON *.* TO 'wordpress'@'%'                    |
| GRANT ALL PRIVILEGES ON `wordpress`.* TO 'wordpress'@'%' |
+----------------------------------------------------------+
2 ROWS IN SET (0.00 sec)
```
