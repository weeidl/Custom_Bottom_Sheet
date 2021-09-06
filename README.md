# Custom Bottom Sheet
 
[![pub package](https://img.shields.io/pub/v/adaptive_action_sheet.svg)](https://pub.dev/packages/custom_bottom_sheet)

A action bottom sheet that adapts to the platform (Android/iOS).

iOS | Android
--- | ---
<img width="520" alt="n1" src="https://github.com/weeidl/Custom_Bottom_Sheet/blob/master/image/video_readmi.gif"> | <img width="497" alt="n2" src="https://github.com/weeidl/Custom_Bottom_Sheet/blob/master/image/photo_readmi.jpg">

## Getting Started

 Add the package to your pubspec.yaml:

 ```yaml
 custom_bottom_sheet: ^1.0.3
 ```
 
 In your dart file, import the library:

 ```Dart
import 'package:custom_bottom_sheet/custom_bottom_sheet.dart';
 ``` 
  Instead of using a `showModalBottomSheet` use `SlideDialog.showSlideDialog` Widget:

  ```Dart
void customBottomSheet(BuildContext context) {
    SlideDialog.showSlideDialog(
      context: context,
      backgroundColor: Colors.white,
      pillColor: Colors.yellow,
      transitionDuration: Duration(milliseconds: 300),
      child: Text('Your code'),
    );
  }
```

### Parameters:
#### showAdaptiveActionSheet:
* `actions`: The Actions list that will appear on the ActionSheet. (required)
* `cancelAction`: The optional cancel button that show under the actions (grouped separately on iOS).
* `title`: The optional title widget that show above the actions.
*  The optional `backgroundColor` and `barrierColor` can be passed in to customize the appearance and behavior of persistent material bottom sheets(Android only).

#### BottomSheetAction:
* `title`: The primary content of the action sheet item. (required)
* `onPressed`: The callback that is called when the action item is tapped. (required)
* `leading`: A widget to display before the title. Typically an Icon widget. (optional)
* `trailing`: A widget to display after the title. Typically an Icon or a CircleAvatar widget. (optional)

#### CancelAction:
* `title`: The primary content of the cancel action sheet item. (required)
* `onPressed`: The callback that is called when the action item is tapped. `onPressed` is optional by default will dismiss the Action Sheet.
