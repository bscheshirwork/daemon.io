### object-storage # ObjectStorage #> ObjectStorage {tpl-git PHPDaemon/Structures/ObjectStorage.php}

Данный класс наследуется от {tpl-outlink http://php.net/manual/class.splobjectstorage.php SplObjectStorage} и предоставляет хранилище объектов с несколькими дополнительными методами.

> Можно создавать классы-наследники ObjectStorage.
> Класс {tpl-inlink network/pool Network/Pool} наследуется от ObjectStorage.

#### methods # Методы

 -.method ```php.inline
 integer public ObjectStorage::each ( string $method, mixed $args, ... )
 ```
   -.n Проходит по всем объектам, вызывая у каждого из них метод `:phc`$method` c заданными аргументами `:phc`$args` и возвращает количество объектов в хранилище
   -.n.ti `:hc`$method` — вызываемый метод объекта
   -.n `:hc`$args` &mdash; аргументы

 -.method ```php.inline
 void public ObjectStorage::removeAll ( object $obj = null )
 ```
   -.n Удаляет из хранилища все объекты.
   -.n.ti `:hc`$obj` &mdash; контейнер, содержащий элементы, которые должны остаться в текущем контейнере

 -.method ```php.inline
 object public ObjectStorage::detachFirst ( )
 ```
   -.n Возвращает первый объект, удалив его из контейнера

 -.method ```php.inline
 object public ObjectStorage::getFirst ( )
 ```
   -.n Возвращает первый объект контейнера