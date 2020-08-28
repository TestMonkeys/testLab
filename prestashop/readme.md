Manual Steps:
db setup:
```
docker exec -it sandbox_mysql mysql -u root -pDBPasswordHere  -e "CREATE DATABASE prestashop1;"
docker exec -it sandbox_mysql mysql -u root -pDBPasswordHere  -e "Create USER 'prestashop1'@'%' IDENTIFIED WITH mysql_native_password BY 'prestashop1';"
docker exec -it sandbox_mysql mysql -u root -pDBPasswordHere  -e "GRANT ALL PRIVILEGES ON prestashop1.* TO 'prestashop1'@'%'"
```

update ssl records in db:
```
UPDATE prestashop1.ps_configuration SET value = '1' WHERE name = 'PS_SSL_ENABLED';
UPDATE prestashop1.ps_configuration SET value = '1' WHERE name = 'PS_SSL_ENABLED_EVERYWHERE';
```