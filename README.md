## Определения

**Entity Description** (NSEntityDescription). Описание сущности. Можно ассоциировать с таблицей в базе данных.

**Managed Object** (NSManagedћObject) - объект, который можно хранить в постоянном хранилище. Состоит из описания сущности (NSEntityDescription) и контекста управляемых объектов (NSManagedObjectContext).

**Managed Object Model** (NSManagedObjectModel). Позволяет описать в приложении сущность, свойства и взаимосвязь между ними и сопоставить записи в постоянном хранилище с управляемыми объектами (Managed Object), которые используются в приложении. Является программным представлением файла .xcdatamodeld в Xcode.

**Managed Оbject Сontext** (NSManagedObjectContext). Состоит из группы связанных объектов модели (Managed Object). Отслеживает изменения и отношения между объектами. Содержат в памяти представления резервных данных.

**Persistent Container** (NSPersistentContainer). Упрощает создание и управление стеком Core Data, обрабатывая создание модели управляемых объектов (NSManagedObjectModel), координатора постоянного хранилища (NSPersistentStoreCoordinator) и контекста управляемых объектов (NSManagedObjectContext).

## Сценарии

#### Тестирование CoreData

Одна модель (NSManagedObjectModel) и разные хранилища

1. Инициализировать рабочий CoreData стек.
2. Создать объект `NSPersistentStoreDescription`
3. Создать объект `NSPersistentContainer` из модели `NSManagedObjectModel` из рабочего CoreData стека.
4. Добавить описание `NSPersistentStoreDescription` в ранее созданный контейнер `NSPersistentContainer`.
5. Выполнить `loadPersistentStores` метод ранее созданного контейнера. 
6. Настроить политику миграций контейнера `automaticallyMergesChangesFromParent`.

#### Не рабочий вариант

Несколько моделей (NSManagedObjectModel) и разные постоянные хранилища.

## Справочная информация

* [Официальное руководство Core Data Programming Guide из архива](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CoreData/index.html#//apple_ref/doc/uid/TP40001075-CH2-SW1).
* [Статья на Хабре  про создание CoreData модели из кода](https://habr.com/ru/articles/498708/).
* [Статья с сайта Kodeco про Unit тесты](https://www.kodeco.com/11349416-unit-testing-core-data-in-ios).
* [Создание CoreData вручную, официальная документация](https://developer.apple.com/documentation/coredata/setting_up_a_core_data_stack/setting_up_a_core_data_stack_manually).
