# at_newversion_notification

A new Flutter project.

* This flutter package alert the user to update the application into a new updated version.
* With the help of an alert pop-up, users can easily navigate to the appropriate Play Store or App Store Page.

## UI
The UI of the alert dialog is simply a card.

Screenshots:

<img src="https://raw.githubusercontent.com/d2itechnology/at_newversion_notification/main/screenshots/both.png?token=AUJGZABAX3TJOUFYSYZY4ATBHGZHW"/>

## Installation
Add at_newversion_notification as [a dependency in your `pubspec.yaml` file.](https://flutter.io/using-packages/)
```
dependencies:
  at_newversion_notification: ^0.0.1
```
## Usage
* In main.dart (or any) file, first create an instance of the `AtNewVersionNotification` class in your `initState()` method.

   `final AtNewVersionNotification atNewVersionNotification = AtNewVersionNotification();`

* Find your application package name and pass the value in `andoidAppId`, `iOSAppId`.

* And Pass application minimum version value in `minimumVersion` parameter.

* Call showAlertDialog method-
  `atNewVersionNotification.showAlertDialog(context: context);`

* Application's `BuildContext` class will check if the app can be updated.

* Based on the platform (Android/iOS) the alert dialog will automatically show. And user can redirect to the app store on the `Update` button click.

## Example
```
 import 'package:flutter/cupertino.dart';
 import 'package:flutter/material.dart';
 import '/at_new_version_notification.dart';

 class Example extends StatefulWidget {
   const Example({Key? key}) : super(key: key);

   @override
   _ExampleState createState() => _ExampleState();
 }

 class _ExampleState extends State<Example> {
   @override
   void initState() {
     super.initState();

     final AtNewVersionNotification atNewVersionNotification =
         AtNewVersionNotification(
             iOSAppId: 'com.google.myride',
             androidAppId: 'com.google.rever',
             minimumVersion: '1.0.0');

     showDialog(atNewVersionNotification);
   }

   void showDialog(AtNewVersionNotification atNewVersion) {
     atNewVersion.showAlertDialog(context: context);
   }

   @override
   Widget build(BuildContext context) {
     return Scaffold(
       body: Container(),
     );
   }
 }
 ```




