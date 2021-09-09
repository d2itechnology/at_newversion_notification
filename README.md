# at_newversion_notification

A new Flutter project.

* This flutter package will alert app users to update the application.
* With the help of an alert pop-up, users can easily navigate to the respective stores(App Store or play Store) to update the app.

## UI
The UI of the alert dialog is simply a card.

Screenshots:

<img src="https://raw.githubusercontent.com/d2itechnology/at_newversion_notification/main/screenshots/both.png?token=AUJGZAF442K3FYYPDTXQGY3BHGT5U"/>

## Installation
Add at_newversion_notification as [a dependency in your `pubspec.yaml` file.](https://flutter.io/using-packages/)
```
dependencies:
  at_newversion_notification: ^0.0.1
```
## Usage
* In main.dart (or any) file, first create an instance of the `AtNewVersionNotification` class in your `initState()` method.

   `final AtNewVersionNotification atNewVersionNotification = AtNewVersionNotification();`

* Pass the application package name in `andoidAppId`, `iOSAppId`.

* Pass application minimum version value in `minimumVersion` parameter. This parameter is used to force people to update application, any user having version less than the specified version will be forced to update application

* Call showAlertDialog method-
  `atNewVersionNotification.showAlertDialog(context: context);`

* If updated app version is available on stores, application will get a popup on launch of application and an option to Update. On click of update button user will be directed to the respective stores(App store or play store).

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




