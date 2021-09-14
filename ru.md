# Используем кнопки
```template
basic.forever(function () {
    
})

```
```blocks
input.onButtonPressed(Button.A, function () {
    
})
```
## Step 0 @showDialog
Привет! Сегодня мы научимся использовать кнопки и напишем программу для игры на реакцию. 

## Step 1 @showHint
### Используем кнопки
Вспомним: мы знаем два способа начать нашу программу, ``||basic.при начале||`` и ``||basic.постоянно||``.  
Обратим внимание на ещё один блок - ``||input.кнопка нажата||``. Он находится на вкладке ``||input.Ввод||``.
```hint
Добавим эту команду в свою программу.
```
```blocks
input.onButtonPressed(Button.A, function () {
    
})
```

## Step 2 @showHint
### Используем кнопки
Пусть Micro:bit покажет весёлое лицо, когда кнопка будет нажата. Соберите программу по образцу, загрузите в Micro:bit и нажмите кнопку``|A|``(слева). Видите картинку на экране?
```hint
Программа может выглядеть так:
```
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showIcon(IconNames.Happy)
})
```
```hint
Или так:
```
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showLeds(`
        . . . . .
        . # . # .
        . . . . .
        # . . . #
        . # # # .
        `)
})
```

## Step 2
### Задание 1
Дополните программу так, чтобы по нажатию второй кнопки `|B|`(справа) Micro:bit отображал грустное лицо. Загрузите вашу программу. Переключаются ли лица по нажатию кнопок?

## Step 3 @showDialog
Обратите внимание: в вашей программе может быть не более 3 активных команд ``||input.кнопка нажата||``. При этом, каждый из блоков ``||input.кнопка нажата||`` должен относиться к разным кнопкам.

## Step 4
### Сделай сам!
Придумайте игру на реакцию с простыми правилами:
* [ ] Если кнопка ``|A|`` нажата, побеждает игрок 1.
* [ ] Если кнопка ``|B|`` нажата, побеждает игрок 2.
* [ ] Если обе кнопки нажаты одновременно, объявляется ничья.
```hint
Эта команда покажет имя игрока: 
```
```block
basic.showString("Player 1 wins!")
```
```hint
Эта команда покажет кубок победителя:
```
```block
basic.showLeds(`
        . # # # .
        # # # # #
        . # # # .
        . . # . .
        . # # # .
        `)
```
## Step 5
Все задания выполнены! Теперь, скачайте программу на Micro:bit и позовите друзей, чтобы поиграть!  
Чтобы узнать больше о том, как работают кнопки, посмотрите [видео](https://www.youtube.com/watch?v=t_Qujjd_38o&list=PLMMBk9hE-SeqDYtw9pGNPsQ10V_EGMyGe&index=2)!

## Answers @showDialog

### Ответ: Задание 1

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showIcon(IconNames.Happy)
})
input.onButtonPressed(Button.B, function () {
    basic.showIcon(IconNames.Sad)
})
```
### Ответ: Сделай сам!
Программа может выглядеть так:
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showString("Alice wins!")
    basic.showLeds(`
        . # # # .
        # # # # #
        . # # # .
        . . # . .
        . # # # .
        `)
})
input.onButtonPressed(Button.B, function () {
    basic.showString("Bob wins!")
    basic.showLeds(`
        . # # # .
        # # # # #
        . # # # .
        . . # . .
        . # # # .
        `)
})
input.onButtonPressed(Button.AB, function () {
    basic.showString("Draw!")
})
```
