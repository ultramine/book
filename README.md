# ULTRAMINE CORE book

**Внимание! Не использовать в продакшене! Текущая версия ядра - 0.1.0-beta, это даже не пререлиз, это пререлиз пререлиза. НЕ ИСПОЛЬЗУЙТЕ ЭТО! DO NOT USE IT!**

Ядро UltraMine - это реализация minecraft сервера на основе MinecraftForge, действительно пригодное для промышленного использования на высоконагруженных серверах с сотнями модов. В отличии от Cauldron, Не реализует Bukkit API и не поддерживает плагины. 

Нигде в этих статьях вы не найдете ни описания ядра, ни чем оно отличается от MinecraftForge. Здесь только прикладная часть: конфигурация, использование, обслуживание. Никакого маркетинга.

* [Быстрый старт](Quickstart.md)
* Конфигурация сервера
  * Базовая настройка сервера - [server.yml](server.yml.md)
  * Настройка миров - [worlds.yml](worlds.yml.md)
  * Настройка пермишанов - [Permissions](Permissions.md)
  * Блокировка предметов - [itemblocker.yml](itemblocker.yml.md)
* [Спавн мобов в UltraMine](MobSpawn.md)

Прочие ссылки:
* [Исходники ядра](https://gitlab.ultramine.ru/ultramine/ultramine_core)
* [Maven репозиторий](https://maven.ultramine.ru/org/ultramine/core)

Известные несовместимости:
* FastCraft
* ServerTools
* ForgeEssentials
* DragonAPI
* zzzzzcustomconfigs
* NEID