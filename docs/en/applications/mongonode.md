### mongonode # MongoNode #> MongoNode {tpl-git PHPDaemon/Examples/MongoNode.php}

```php:p
namespace PHPDaemon\Examples;
class MongoNode;
```

Это приложение предоставляет узел репликации MongoDB. Это дает возможность устанавливать произвольные хуки на добавление/изменение/удаление объектов.

#### requirements # Требования

Требуется установленный модуль pecl/mongo и включенный phpdaemon/MongoCllient.

#### use # Использование

Когда MongoNode включено, оно незамедлительно получает новые изменения в базе.

По-умолчанию:

Если объект обладает свойством “_key” сериализованное его значение отправляется в ключ Memcache под тем названием, которое задано в значении _key. Когда объект удаляется из MongoDB, он удаляется и из Memcache.

Если объект имеет свойство “_ev”, его значение отправляется в RTEP-событие под тем названием, которое задано в значении _ev.