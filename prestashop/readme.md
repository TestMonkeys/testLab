Manual Steps:
update ssl records in db:
```
UPDATE prestashop1.ps_configuration SET value = '1' WHERE name = 'PS_SSL_ENABLED';
UPDATE prestashop1.ps_configuration SET value = '1' WHERE name = 'PS_SSL_ENABLED_EVERYWHERE';
```