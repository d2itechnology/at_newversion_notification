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
  new_version: ^0.0.1
```
## Usage
In main.dart file, first create an instance of the `AppNewVersion` class.
Then Find your application package name and pass the value in andoidAppId and iOSAppId.

For iOS, If your app is only available outside the U.S. App Store, then you should pass a two-letter country code in iOSAppStoreCountry. You can search the country code for a specific country.

You can call the `showAlertDialogIfRequired` method in your Build Context, with the help of this a popup will automatically show based on your platform.


