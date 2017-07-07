`settings/server.yml` - Базовый конфиг ядра. Полностью заменяет ванильный `server.properties` и также содержит другие опции. Синтаксис конфигурации - [YAML](https://ru.wikipedia.org/wiki/YAML).

```yaml
listen:
    minecraft:
        serverIP: '' #IP minecraft сервера. Оставить пустым для любого IP (vanilla)
        port: 25565 #Порт minecraft сервера (vanilla)
    query: #UT4 Query для распространения информации о сервере (статус доступности, онлайн). Может занимать тот же порт, что и minecraft (vanilla)
        enabled: false 
        port: 25565
    rcon: #Удаленная консоль. НЕ может занимать тот же порт, что и minecraft. (vanilla)
        enabled: false
        port: 25566
        password: ''
settings:
    authorization:
        onlineMode: true #Ванильный onlineMode. Поставить false для отключения авторизации и допуска пиратских клиентов (vanilla)
    player:
        playerIdleTimeout: 0 #AFT автокик. Время простоя в секундах, по истечению которого игрока кикнетс сервера (vanilla)
        gamemode: 0 #Гейммод по умолчанию. 0 - survival, 1 - creative (vanilla)
        maxPlayers: 20 #Кол-во слотов (vanilla)
        allowFlight: false #Ванильный античит от полетов (vanilla)
        forceGamemode: false #Восстанавливать гейммод по умолчанию при каждом входе игрока на сервер (vanilla)
        whiteList: false #Включение/выключение вайтлиста (vanilla)
    other:
        snooperEnabled: true #Отсылать статистику работы сервера разработчикам в Mojang (vanilla)
        hardcore: false #Без комментариев (vanilla)
        resourcePack: '' #Имя ресурспака по умолчанию. Будет отправлен клиенту при первом входе на сервер (vanilla)
        enableCommandBlock: false #Влючение/выключение командных блоков (vanilla)
        splitWorldDirs: true #Использовать новое расположение миров по директориям. Поставить false для использования ванильной разметки
    spawnLocations:
        firstSpawn: spawn #Варп, на который игрок попадает при первом входе на сервер
        deathSpawn: spawn #Варп, на который игрок попадает при смерти
        respawnOnBed: true #Возрождаться на кроватях (а не на варпе, который указан выше)
    teleportation:
        cooldown: 60 #Время (в секундах) между использованием телепортации (/home /spawn и т.п.)
        delay: 5 #Задержка (в секундах) перед телепортацией после введения команды
        interWorldHome: true #Разрешить телепортацию /home между мирами
        interWorldWarp: true #Разрешить телепортацию /warp между мирами
    messages:
        announcePlayerAchievements: true #Выписывать в чат каждую полученную ачивку (vanilla)
        motd: A Minecraft Server #Описание сервера, показывается в списке серверов клиента (vanilla)
    watchdogThread:
        timeout: 120 #Если сервер завис и не отвечает указанное количество секунд, то будут выписаны стактрейсы всех потоков, и...
        restart: true #... если установелно true, сервер будет убит
    security:
        checkBreakSpeed: true #Если поставить false, сервер не будет проверять время разрушения блока. От этого он может стать уязвимее перед хакерскими атаками, но при сильных лагах блоки будут разрушаться с той же скоростью
tools:
    autobroadcast: #Автосообщения
        enabled: false
        intervalSeconds: 600 #Интервал между сообщениями
        messages: [] #Список сообщений (выписываются по очереди)
        showAllMessages: false #Если true, то выписываются все сразу
    autoDebugInfo: #Автосообщения о нагрузке и состоянии сервера (выписываются в консоль и людям с соответствующими пермишанами)
        enabled: true
        intervalSeconds: 600
    autobackup: #Автобэкап миров
        enabled: false
        interval: 60 #Интервал между бэкапами (в минутах)
        maxBackups: 10 #Максимальное количество бэкапов в папке (будут удаляться самые старые)
        maxDirSize: 50000 #Максимальный размер папки с бэкапами (в мегабайтах) (будут удаляться самые старые)
        worlds: null #Список миров для бэкапа (null, если нужно бэкапить все)
        notifyPlayers: true #Уведомлять игроков о начале выполнения бэкапа
```