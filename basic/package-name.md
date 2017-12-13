# Changing Application Package Name

In this tutorial, we will show how to use AppyBuilder that allows you to change the application package name for an app which contains multiple screens.

**Scenario:** You may have an app that was developed in MIT AI and published to Google Play Store. MIT AI uses package naming convention of **appinventor.ai\_YourEmail.YourAppName **\(where **YourEmail **is your google email e.g. jdoe01\). You can easily import this app into AppyBuilder, but that will cause the package name to be changed to AppyBuilder default package name. For this reason, we can use feature below to use same package name that was used in MIT AI.

**Process:**In this tutorial we’ll create a simple app called **testapp** that will include 2 screens. We will change AppyBuilder default package name and will include a Button to switch from Screen1 to Screen2.

Image below shows how to change the default package name using **ApplicationPackage**property \(_only visible to Scrreen1 – will globally apply to entire app_\). For this exercise, let’s name our app _testapp_ and attempt to change default package-name to_com.example.testapp_ as shown below. Also, let’s assume your email is jdoe@gmail.com

![](https://i0.wp.com/community.appybuilder.com/uploads/default/optimized/1X/864c3204070536be123688bb996c750ceaf55362_1_690x326.png)

Our simple app includes a button and clicking the button should start Screen2. The blocks to accomplish this is shown in image below. When opening another screen, we use the following convention:

**emailusername.projectname.screenname**

* Replace “projectname” to the “
  **name of the project**
  ”
* Replace “emailusername” to the “
  **username of your email**
   \(text before @\). Also, if your username includes dot \(e.g. jdoe.01@gmail.com, replace . to \_ like jdoe\_01\)
* Replace “screenname” to 
  **“the screen you want to open**
  “

![](https://i0.wp.com/community.appybuilder.com/uploads/default/optimized/1X/8d5681ae9151bcb41c4c02e79ed6da9cd35ff4b1_1_690x135.png)

This approach will properly work when you have built .apk. However, when using companion to test you could use approach below \(thanks [**Boban**](http://community.appybuilder.com/u/boban_stojmenovic) for his input\):

![](https://i2.wp.com/community.appybuilder.com/uploads/default/original/2X/6/63ef0ebe87c28266255f99cc51bb7ecdae585076.png "image")

