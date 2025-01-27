Curso de SQL basico en MySQL
---

# Iniciar MySQL

```bash
docker run --name mysql -e MYSQL_ROOT_PASSWORD=admin -p 3306:3306 -d mysql:8
```

Otra forma de iniciarlo es compartiendo el directorio donde estamos con el contenedor:

```bash
docker run --name mysql -e MYSQL_ROOT_PASSWORD=admin -p 3306:3306 --volume $(pwd)/:/root -d mysql:8
```

NOTA: Puede que reinicies el equipo y el contenedor se detenga, puedes iniciarlo de la siguiente manera:

```bash
docker start mysql
```

## Entrar en el MySQL:

```
docker exec -it mysql mysql -h 127.0.0.1 -uroot -padmin
```

## Entrar en la instancia de MySQL

```
docker exec -it mysql /bin/bash
```

## Entrar al MySQL teniendo el cliente en local instalado:

```
mysql -h 127.0.0.1 -u root -padmin
```

## Hacer un respaldo:

```
mysqldump -h 127.0.0.1 -u root -padmin demo > demo.sql
```

## Restaurar un respaldo:

```
mysql -h 127.0.0.1 -u root -padmin < demo.sql
```

## Clientes gratuitos para conectarse al MySQL

- [mysql-Cliente](https://dev.mysql.com/downloads/mysql): Cliente nativo en la terminal.
- [MySQL Workbench](https://dev.mysql.com/downloads/workbench): Cliente gráfico oficial de MySQL.
- [Sequel Pro](https://sequelpro.com)
- [DBeaver](https://dbeaver.io/download)
- [HeidiSQL](https://www.heidisql.com)

## Material

- https://www.mysqltutorial.org
- https://use-the-index-luke.com
- https://dev.mysql.com/doc/refman/8.0/en
- https://debeando.com
- https://db-engines.com/en/ranking
