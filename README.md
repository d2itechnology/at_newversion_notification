# at_newversion_notification

A new Flutter project.

This flutter package alert the user to update the application into a new updated version.
With the help of an alert pop-up, users can easily navigate to the appropriate Play Store or App Store Page.

## UI
The UI of the alert dialog is simply a card.

## Installation
Add new_version as [a dependency in your `pubspec.yaml` file.](https://flutter.io/using-packages/)
```
dependencies:
  at_newversion_notification: ^0.0.1
```
## Usage
In main.dart file, first create an instance of the `AtNewVersionNotification` class.
`final atNewVersionNotific = AtNewVersionNotification();`

Then Find your application package name and pass the value in andoidAppId, iOSAppId and
pass `minimum version` in minimumVersion parameter.

And calling `showAlertDialog` method with your app. `BuildContext` will check if app is applicable for updates or not. And based on platform the alert dialog will automatically open then user can go to the app store.

`atNewVersionNotific.showAlertDialog(context: context);`




