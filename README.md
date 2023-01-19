# drupal-local

# Requerimientos para ejecutar drupal-local
 
 Nginx 
 PHP = 8.1.12 o >
 MariaDB = 10.4.27 o >
 
# habilitar las extensiones de php dg y dom
 
 Se debe crear una base de datos e importar el archivo drupal.sql y establecer la configuración en el archivo settings.php ubicado en la ruta
 drupal-local\web\sites\default en la linea 816, establecer los valores de configuración a la base de datos segun corresponda:
 
 $databases['default']['default'] = array (
  'database' => 'drupal_local',
  'username' => 'root',
  'password' => '',
  'prefix' => '',
  'host' => 'localhost',
  'port' => '3306',
  'namespace' => 'Drupal\\mysql\\Driver\\Database\\mysql',
  'driver' => 'mysql',
  'autoload' => 'core/modules/mysql/src/Driver/Database/mysql/',
);

Una vez configurado lo anteriormente indicado, ya es posible ingresar a localhost/drupal y verficar su ya esta cargando el sitio. es posible consumir desde un cliente como postman el siguiente endpoint tipo GET http://localhost/drupal-local/web/api/v1/articles
el cual requiere una autenticación Basic Auth con las siquientes credenciales Username: admin  password: pRiaUgjTiy

el cual, regresa todos los nodos de tipo artículo.

Asimismo se tiene el sitio con todas sus funcionalidades. para poder acceder como usuario administrador se tienen la siguientes credenciales:
User name: admin  User password: pRiaUgjTiy
