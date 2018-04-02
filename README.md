# Codeigniter Database Config Helper
`New member of the old world`

Usage
-----

Include:
```php
  $this->load->helper('config');
```
Simple use:
```php
  echo table('users');
  ## output: USERS
  
  echo table('users', 'username');
  ## output: USERS.USERNAME
  
  $select = array(
    array( 'users', 'fullname' ),
    array( 'users', 'pass', 'password' ),
    array( 'options', 'value', 'val' )
  );
  echo table( $select );
  ## output: USERS.FULL_NAME, USERS.PASSWORD AS password, OPTIONS.VALUE AS val
```

Exmaple Mysql
-----
#### OPTIONS Table
```sql
+----------+-------------+----------------+
|       ID | NAME        | VALUE          |
+----------+-------------+----------------+
|        1 | HOME        | www.site.com   |
|        2 | SUG         | AHMETTASHAN    |
+----------+-------------+----------------+
```
#### USERS Table
```sql
+----------+-------------+----------------+----------------+
|       ID | USERNAME    | FULL_NAME      | PASSWORD       |
+----------+-------------+----------------+----------------+
|        1 | ahmet       | Ahmet Tashan   | 123456seven    |
|        2 | serdar      | Serdar Yalın   | 123456seven    |
|        3 | pland       | Phil Toland    | 123456seven    |
+----------+-------------+----------------+----------------+
```
