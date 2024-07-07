## Определения

**Entity Description** (NSEntityDescription). Описание сущности. Можно ассоциировать с таблицей в базе данных.

**Managed Object** (NSManagedћObject) - объект, который можно хранить в постоянном хранилище. Состоит из описания сущности (NSEntityDescription) и контекста управляемых объектов (NSManagedObjectContext).

**Managed Object Model** (NSManagedObjectModel). Позволяет описать в приложении сущность, свойства и взаимосвязь между ними и сопоставить записи в постоянном хранилище с управляемыми объектами (Managed Object), которые используются в приложении. Является программным представлением файла .xcdatamodeld в Xcode.

**Managed Оbject Сontext** (NSManagedObjectContext). Состоит из группы связанных объектов модели (Managed Object). Отслеживает изменения и отношения между объектами. Содержат в памяти представления резервных данных.

**Persistent Container** (NSPersistentContainer). Упрощает создание и управление стеком Core Data, обрабатывая создание модели управляемых объектов (NSManagedObjectModel), координатора постоянного хранилища (NSPersistentStoreCoordinator) и контекста управляемых объектов (NSManagedObjectContext).

## Сценарии

1. Создать объект Managed Object Model (NSManagedObjectModel).
2. Создать Persistent Container (NSPersistentContainer).
3. Получить из Persistent Container объект ManagedObjectContext.
4. Объект Managed Object Context является основным для работы.

## Справочная информация

1. Официальное руководство Core Data Programming Guide из архива [https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CoreData/index.html#//apple_ref/doc/uid/TP40001075-CH2-SW1](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CoreData/index.html#//apple_ref/doc/uid/TP40001075-CH2-SW1)
2. Статья на Хабре "CoreData модель из кода". [https://habr.com/ru/articles/498708/](https://habr.com/ru/articles/498708/)
