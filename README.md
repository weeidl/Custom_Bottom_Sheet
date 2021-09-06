# Custom Bottom Sheet
 
[![pub package](https://img.shields.io/pub/v/adaptive_action_sheet.svg)](https://pub.dev/packages/custom_bottom_sheet)

A action bottom sheet that adapts to the platform.

Video | Photo
--- | ---
<img width="520" alt="n1" src="https://github.com/weeidl/Custom_Bottom_Sheet/blob/master/image/video_readmi.gif"> | <img width="520" alt="n2" src="https://github.com/weeidl/Custom_Bottom_Sheet/blob/master/image/photo_readmi.jpg">

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
#### SlideDialog.showSlideDialog:
* `pillColor`: Color for the yellow label at the top of the model sheet.
* `backgroundColor`: The background of everything is set SlideDialog.showSlideDialog.
* `transitionDuration`: The time of the animation of the appearance and closing.
* `child`: Pass here the widgets that you want to display.
