_**TODO:**_
1. _Incorporate materials from [programming notebooks](https://github.com/CE-Curriculum-Development/mat-cpe-1040)._  
2. _Rearrange for the _study, apply, present_ structure like [CE Learning Progression 006: Flip-flops](https://github.com/ivogeorg/https://github.com/ivogeorg/ce-learning-progression-006-flip-flops)._  
3. Steps:
   1. One-statement progra4
   ```javascript
   basic.showIcon(IconNames.Heart)
   ```
   2. Comments
   ```javascript
   basic.showIcon(IconNames.Heart)       // not executed
   ```
   3. Sequential execution
   ```javascript
   basic.showIcon(IconNames.Heart)
   basic.pause(2000)
   basic.showIcon(IconNames.Butterfly)
   ```
   4. Encapsulation
   ```javascript
   {
       basic.showIcon(IconNames.Heart)
       basic.pause(2000)
       basic.showIcon(IconNames.Butterfly)
   }
   ```
   5. Conditionals
   ```javascript
   if (true) {
       basic.showIcon(IconNames.Heart)
       basic.pause(2000)
       basic.showIcon(IconNames.Butterfly)
   } else {
       basic.showIcon(IconNames.Angry)
       basic.pause(2000)
       basic.showIcon(IconNames.Snake)
   }
   
   if (false) {
       basic.showIcon(IconNames.Heart)
       basic.pause(2000)
       basic.showIcon(IconNames.Butterfly)
   } else {
       basic.showIcon(IconNames.Angry)
       basic.pause(2000)
       basic.showIcon(IconNames.Snake)
   }
   ```
   6. Data types
   ```javascript
   let isHeart : boolean = true

   if (isHeart) {
       basic.showIcon(IconNames.Heart)
       basic.pause(2000)
       basic.showIcon(IconNames.Butterfly)
   } else {
       basic.showIcon(IconNames.Angry)
       basic.pause(2000)
       basic.showIcon(IconNames.Snake)
   }
   ```
   7. Functions
   ```javascript
   function displayIcons(isHeart : boolean) {
       if (isHeart) {
           basic.showIcon(IconNames.Heart)
           basic.pause(2000)
           basic.showIcon(IconNames.Butterfly)
       } else {
           basic.showIcon(IconNames.Angry)
           basic.pause(2000)
           basic.showIcon(IconNames.Snake)
       }
   }
   
   displayIcons()
   ```
   8. Loops
   ```javascript

   while (true) {
       basic.showIcon(IconNames.Heart)
       basic.pause(2000)
       basic.clearScreen()
   })
   ```
   9. Loop function
   ```javascript

   basic.forever(function () {
       basic.showIcon(IconNames.Heart)
       basic.pause(2000)
       basic.clearScreen()
   })
   ```
   10. Inside and outside of loops
   ```javascript
   let isHeart : boolean = true

   basic.forever(function () {
       if (isHeart) {
           basic.showIcon(IconNames.Heart)
       } else {
           basic.showIcon(IconNames.Butterfly)
       }
       basic.pause(2000)
       basic.clearScreen()
   })
   ```
   11. Events
   ```javascript
   let isHeart : boolean = true
   
   input.onButtonPressed(Button.A, function () {
       if (isHeart) {
           isHeart = false
       } else {
           isHeart = true
       }
   })

   basic.forever(function () {
       if (isHeart) {
           basic.showIcon(IconNames.Heart)
       } else {
           basic.showIcon(IconNames.Butterfly)
       }
       basic.pause(2000)
       basic.clearScreen()
   })
   ```
   12. Flipping a boolean
   ```javascript
   let isHeart : boolean = true
   
   input.onButtonPressed(Button.A, function () {
       uprightHeart = !uprightHeart
   })

   basic.forever(function () {
       if (isHeart) {
           basic.showIcon(IconNames.Heart)
       } else {
           basic.showIcon(IconNames.Butterfly)
       }
       basic.pause(2000)
       basic.clearScreen()
   })
   ```
---

# CPE 1040 - Spring 2020

This is the first learning progression for the Fall 2020 installment of the CPE 1040 - Intro to Computer Engineering course at MSU Denver.

Table of Contents
=================

**TODO**


## Learning Progression 001: micro:bit

This progression will just familarize you with the environment we'll use: Microsoft Teams, Github Classroom, and Microsoft Makecode. All the activities will be shown and LA-ed in the lab, including submitting the assignment. Programming in JavaScript will be shown, as well as editing Markdown files, like this [README](README.md).

### Step 1: Basic
1. In [Makecode](https://makecode.microbit.org/), create a new project.
2. In the editor, select JavaScript. **Note:** We will not be using Blocks!
3. In the box, where _Untitled_ is shown, write _basic-program_.
4. In the editor on the right, write an infinite loop (aka `forever` loop).
5. In the loop, write the following code:
   1. Show the _Heart_ icon.
   2. Pause for 0.1 s (= 100 ms). The argument has to be in ms.
   3. Clear the screen.
6. In the simulator on the left verify that the heart is "beating".

### Step 2: Button
1. Create a _boolean_ variable, called `iconHeart`. Boolean variables hold one of two values: `true` or `false`. Set the initial value to `true`.
2. Create a _button handler_. Choose the A button in the first argument.
3. In the handler function body, write one line of code, which flips the `iconHeart` variable. That is, if it is `true`, it flips it to `false`, and vice versa.
4. In the infinite loop, write an `if ... else` statement, with curly braces.
5. In the condition (parentheses right next to the `if`), put the `iconHeart` variable.
6. Move the line that shows the icon _inside_ the curly braces of the `if` block.
7. In the block of the `else` statement, Write a similar line which shows the _Butterfly_ icon.
8. In the simulator, where the heart is "beating", click the A button, and verify that the butterfly is "flapping". Click the A button again to return to the heart.

### Step 3: micro:bit
1. Connect your micro:bit to your computer using the short USB cable.
2. On the desktop, and icon will appear for the connected device. Alternatively (on Windows), a new "drive" will be shown in the file explorer.
3. In Makecode, click on the Download button. This will _compile_ your program and convert it to a format (_hexadecimal_ numbers) that the micro:bit can execute.
4. Find the file in your file system. If you followed the instructions above, the file will be called _microbit-basic-program.hex_.
5. Drag the file onto the micro:bit icon or drive. This will write the file onto the micro:bit device, after which it will start executing. Verify that the heart is beating, and you can switch to the flapping butterfly, and back to the heart.

### Step 4: Source file
1. Follow the assignment URL provided in Teams. 
2. If you haven't created a Github account yet, you will be asked to do so. Follow the instructions. _Note: You have been invited with your MSU email._
3. Click on the **Accept assignment** button. This will create your own copy of the assignment repository. These instructions will show, as the README.md file at the top level of each repository is rendered and displayed below the file listing.
4. Click on the **Create new file** button. This will open an editor and a box for a filename.
5. In the filename box, write the name `microbit-basic-program.js`. Note the `js` extension for JavaScript.
6. From Makecode, copy the program and paste it into the open Github editor.
7. Scroll down and click the **Commit** button. This will create a new file with the specified name in your repository. This is called a _source file_. Source files contain the programs in human-readable form.
8. Submit the assignment.

### Step 5: README
1. Open the [README](README.md) file by first clicking on the filename and then clicking the "pencil" icon. You will see the file in _markdown_ format. Note the `md` extension. This is an easy language for formatting the text with highlights, headings, links, images, etc. Refer to the [Github markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) for the most common features.
2. Create item 3 below **in bold**. Create item 4 below _in italic_. Scroll up and click the **Preview** button. The file will be rendered with the changes highlighted. Commit the file.

