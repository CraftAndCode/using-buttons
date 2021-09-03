# Using buttons
```template
basic.forever(function () {
    
})

```
```blocks
input.onButtonPressed(Button.A, function () {
    
})
```
## Step 0 @showDialog
Hello! Today, you'll learn how to use buttons and assemble the code for a reaction-based game. 

## Step 1 @showHint
### Using buttons
You've already learned  two ways of running your program: ``||basic.on start||`` and ``||basic.forever||``.  
Now let's have a look at the ``||input.on button pressed||`` block. You can find it in your toolbox inside the ``||input.input||`` category.
```hint
Find this block and add it to your code.
```
```blocks
input.onButtonPressed(Button.A, function () {
    
})
```

## Step 2 @showHint
### Using buttons
Now, let's make our Micro:bit display a happy face when a button is pressed. When your code is assembled, download it to your Micro:bit and press the ``|A|`` button. Do you see a happy face?
```hint
Your code might look like this:
```
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showIcon(IconNames.Happy)
})
```
```hint
or like this:
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
### Challenge 1
Add your own code to show a sad face when the other button is pressed. Download your code and push the buttons to switch between emotions!

## Step 3 @showDialog
Note that only one program can be assigned to each button. You can also assign a program to both buttons being pressed at once. This means you can't have more than 3 ``||input.on button pressed||`` blocks in your code.

## Step 4
### Now it's your turn
Create a reaction-based game. The rules of the game are simple:
* [ ] If the ``|A|`` button is pressed first, the first player wins.
* [ ] If the ``|B|`` button is pressed first, the second player wins.
* [ ] If the both buttons are pressed at once, a draw is declared.
```hint
You can use this block to display the players' names: 
```
```block
basic.showString("Player 1 wins!")
```
```hint
You can use this block to show a picture of a trophy:
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
Assembled your game? You rock! Now download your code to Micro:bit and play the game with your friends and family!  
  
If you'd like to learn more about how buttons work, [watch this video](https://www.youtube.com/watch?v=t_Qujjd_38o&list=PLMMBk9hE-SeqDYtw9pGNPsQ10V_EGMyGe&index=2)!

## Answers @showDialog

### Answer: Tutorial 1

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showIcon(IconNames.Happy)
})
input.onButtonPressed(Button.B, function () {
    basic.showIcon(IconNames.Sad)
})
```
### Answer: Do it yourself
Your code could be something like this:
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
