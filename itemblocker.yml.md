### Пример файла itemblocker.yml
```yaml
global: #Запреты для всех миров
-   item: 'BuildCraft|Factory:pumpBlock:*' #ID:подID предмета
    useItem: true #Запрещать использование предмета (правый клик)
    useBlock: true #Запрещать использование блока, установленного в мире
    rmItem: true #Удалять блок из инвентаря или любого контейнера, открытого игроком
    rmBlock: true #Удалять блок из мира при попытке активации игроком (правый клик)
-   item: 'IC2:blockMachine:8'
    useItem: true
worlds:
    '-1': #ID мира
        list:
        -   item: 'IC2:blockMachine:8' #Все то же самое, но в конкретном мире
            useItem: true
```