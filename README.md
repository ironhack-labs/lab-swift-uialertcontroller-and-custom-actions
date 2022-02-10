
![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | UIAlertController and custom actions

<br>

## Introduction

In this lab, we will create a small app that allows you to pick and display your favorite food! This one-screen app will have a Label, Image View and a Button. On the button tap, the user will be presented with an alert dialog, with the ability to choose from a few different food options. Once an option is picked, the corresponding image will appear, as well as a description string.

After completing this lab, you will be able to:

- Create alert dialogs with UIAlertController
- Create custom alert dialog button actions with UIAlertAction and define their behavior using closures
- Build a UI that responds to user actions when tapping alert dialog buttons

## Requirements

- Fork this repository.
<!-- - Add your instructor and the class graders to your repository and ensure that your repository is private. Public repositories will receive a zero on the assignment.
  - If you are unsure who your class graders are, ask your instructor or refer to the day 1 slide deck. -->
- Upload the code for all of the following prompts to your repository.

## Submission

- Upon completion, run the following commands:

  ```shell
  git add .
  git commit -m "done"
  git push origin main
  ```

- Create a Pull Request

When you make pull request in pair-programming: `student1,student2-nameOfTheExercise` <br>
When you make a pull request in individual-programming: `student-nameOfTheExercise`

<br>

## Starter code

No starter code needed/provided.

<br>

## Iterations

### Iteration 1

- Create a new Xcode iOS app project
- Add a Label, Image View and a Button to the View Controller Scene
- Setup the Constraints of all the UI elements correctly
- Create appropriate class properties (IBOutlets) and connect them to the UI elements in the Storyboard
- Set the Label's text to "Choose your food.", either programmatically or within the Interface Builder

### Iteration 2

Create an IBAction function that triggers on button tap and implement the following logic:
- Create a new UIAlertController property of type `.alert` and give it a title and a message
- Create at least 2 UIAlertActions with style `.default`. Set each action title to a specific food. On the button tap for both of these actions, change the Label on the screen to say which food has been picked. Also, set the image of the Image View to the image of the picked food. Go online and download pictures you want to use and add them to your Assets catalog.
- Create 1 UIAlertAction with style `.cancel` and title "Cancel" and an action handler of nil
- Add all of these actions to the UIAlertController
- Present the UIAlertController

### Iteration 3

Within the IBAction function, add the following logic:
- Create 1 UIAlertAction with style `.destructive` and title "Delete". Add an action handler that will reset the Label on the screen to its default string and remove the image from the Image View by setting it to nil.

### Iteration 4

- Create a new method `showAlert` with 1 input parameter of type `UIAlertController.Style`
- Move the logic from IBAction to the new method and set its `preferredStyle:` input parameter to the method's input parameter
- Call the new method from the IBAction with setting the value of `UIAlertController.Style` input parameter to `.alert`

### Iteration 5 (Bonus)

- Add another Button below the first one within the Storyboard
- Implement an IBAction function for the new button tap
- Call `showAlert` method from it, setting the value of `UIAlertController.Style` input parameter to `.actionSheet`

<br>

Happy coding! :heart: