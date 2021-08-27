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
Hello! Today you'll learn to use buttons and assemble the code of a reaction-based game. 

## Step 1 @showHint
You've already learned the two ways of running your program: ``||basic.on start||`` and ``||basic.forever||``.  
Now let's have a look at the ``||input.on button pressed||`` block. You can find it in your toolbox inside the ``||input.input||`` category.
```hint
Find this block and add it to your code.
```
```blocks
input.onButtonPressed(Button.A, function () {
	
})
```

## Step 2 @showHint
Now, let's make our Micro:bit display a happy face when a button is pressed. When your code is assembled, download it to your Micro:bit and press the ``|A|`` button. Do you see a happy face?
```hint
Your code could look like this:
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
### Do it yourself
Add your own code to show a sad face when the other button is pressed. Download your code and push buttons to switch between emotions!
```hint
Your code could be something like this:
```
```blocks
input.onButtonPressed(Button.A, function () {
	basic.showIcon(IconNames.Happy)
})
input.onButtonPressed(Button.B, function () {
	basic.showIcon(IconNames.Sad)
})
```
## Step 3 @showDialog
Note, only one program can be assigned to each button. Also, you can assign a program to both buttons being pressed at once. Therefore, you can't have more than 3 ``||input.on button presssed||`` blocks in your code.

## Step 4
### Do it yourself
Make a reaction-based game. The rules of the game are simple:
* [ ] If the ``|A|`` button is pressed first, the first player wins.
* [ ] If the ``|B|`` button is pressed first, the second player wins.
* [ ] If the both buttons are pressed at once, the draw is declared.
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
Assembled your game? You rock! Now go play it with your friends and family!  
  
If you want to learn more about how buttons work, watch this 




