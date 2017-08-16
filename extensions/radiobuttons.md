# Presidents Quiz using RadioButtons

###### This tutorial uses RadioButtons extension that can be downloaded [HERE](http://community.appybuilder.com/t/about-the-extensions-category/2)

This extension allows you to create **RadioButtons **either vertically \(default\) or horizontally within a **HorizontalArrangement **Layout. In this tutorial, we'll create a simple President-Quiz that will look like below. When each **Button **is clicked, we will check the response and show message using **Notifier **component. 

**Get .apk **[**HERE **](http://AppyBuilder.com/tutorials/radiobutton/TutRadioButtons.apk)**and .aia **[**HERE**![](/assets/radiobutton-1.png)](http://AppyBuilder.com/tutorials/radiobutton/TutRadioButtons.aia)

Create a new project. Once project opens, in the **Design Editor**, select the Extensions category and import **RadioButtons **extension. Our sample quiz-app, has 3 questions, each having their own radiobutton possible answers. For each **RadioButtons **component, you can change the **TextColor **and **TextSize**. Customize is as you needed. Also, as shown in image BELOW, we use 3 HorizontalArrangement component. Each of these layouts will be used to hold one-set of responses as shown ABOVE. We use **Labels **to display quiz text and a **Button **to check answer and show status using a **Notifier **component.

![](/assets/rb-quiz-2.png)

We now use Blocks Editor to code the app behavior.  We use **Screen1 Initialize Event **block, to create or radio buttons using **CreateRadioButtons **block. Specify a unique numeric **id **for for each set of radiobuttons, a container, the way that you like to present the radio-buttons \(vertical vs. horizontal\) and **List **of values for each radio-button.![](/assets/rb-quiz-3.png)

We now need to check answer for the "Check Answer" button is pressed for each group. To simplify the logic, eliminate redundancy, we use a **procedure **that accepts 2 **parameters. **First parameter for checking what user has selected and 2nd parameter for receiving the correct response. To determine which radio-button user has selected, we use **RadioButtons.GetChecked** block. This block returns the text of selected radio-button. If nothing selected, a **-1** will be returned. For **Button1**, to check answer, in its **Click **event, we invoke our procedure, passing it **RadioButtons1.GetChecked** \(gets text of selected radio-button for RadioButtons1 group\) and for 2nd parameter, we pass it the correct answer. Our procedure now checks to see if parameter responseText is equal to CorrectAnswer and display an Alert accordingly

![](/assets/rb-quiz-4.png)

