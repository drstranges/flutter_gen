## 4.1.0

**Feature**
- [#138](https://github.com/FlutterGen/flutter_gen/pull/138) Generate dartdoc as follows.
  ```dart
  /// File path: pictures/chip5.jpg
  AssetGenImage get chip5 => const AssetGenImage('pictures/chip5.jpg');
  /// Color: #979797
  static const Color gray410 = Color(0xFF979797);
  ```
- [#143](https://github.com/FlutterGen/flutter_gen/pull/143) Support [Rive](https://rive.app/) files type. 
  ```yaml
  flutter_gen:
    integrations:
      rive: true
  ```
- [#150](https://github.com/FlutterGen/flutter_gen/pull/150) Added the --version option for command-line.
  ```shell
  % fluttergen --version 
  FlutterGen v4.1.0
  ```
**Bug fix**
- [#134](https://github.com/FlutterGen/flutter_gen/pull/134) Added the ability to support the at symbol (@) in file names.
  ```dart
  AssetGenImage get logo2x => const AssetGenImage('assets/images/logo@2x.png');
  ```
**Development**
- Update to Dart 2.14.4.
- Update to Flutter 2.5.3.
- Replace to renovate.

## 4.0.1

**Bug fix**
- [#134](https://github.com/FlutterGen/flutter_gen/issues/134) Support the at symbol (@) in file names.
- [#139](https://github.com/FlutterGen/flutter_gen/issues/139) Error: Method not found: '$checkedCreate

**Development**
- Replace to flutter_lints.

## 4.0.0

**Features**
- [BREAKING] Ended support for Non null safety codes.
- Use for `line_length` instead of `lineLength`.


**Development**
- Replace to [Melos](https://pub.dev/packages/melos).
- Add VSCode setting.

## 3.1.2

- [#117](https://github.com/FlutterGen/flutter_gen/issues/117) Update to analyzer 2.0.0.  
[flutter_gen_runner (flutter_gen_core) 3.1.2 -> analyzer 2.0.0 workaround](https://github.com/FlutterGen/flutter_gen/issues/121)
  ```yaml
  dependency_overrides:
    meta: ^1.7.0
  ```

- [#110](https://github.com/FlutterGen/flutter_gen/pull/110) Replace null safety dart style package.  

## 3.1.1

**Features** & **Bug fix**
- [#103](https://github.com/FlutterGen/flutter_gen/pull/103) Add option packageParameterEnabled to control whether to generate package parameter for assets or not.  

## 3.1.0

**Features**  
- [#98](https://github.com/FlutterGen/flutter_gen/pull/98) Support for adding assets from a package  


## 3.0.0, 3.0.1, 3.0.2

- Support Null Safety
```yaml
flutter_gen:
  output: lib/gen/
  line_length: 80
  null_safety: true # Optional (default: true)
```

## 2.0.1, 2.0.2, 2.0.3

- Update dependencies

## 2.0.0

New Feature
- [BREAKING CHANGE] [#49](https://github.com/FlutterGen/flutter_gen/issues/49) [#53](https://github.com/FlutterGen/flutter_gen/issues/53) Name collision with flutter localization when using build_runner
  ```yaml
  # Before
  # dev_dependencies:
  #  flutter_gen: 1.3.1
  
  # After
  dev_dependencies:
    flutter_gen_runner: ^2.0.0
  ```
- [#74](https://github.com/FlutterGen/flutter_gen/issues/74) Doesn't generate assets.gen.dart when there are no assets
  ```yaml
  flutter_gen:
    fonts:
      enabled: false
  ```
- [#59](https://github.com/FlutterGen/flutter_gen/issues/59) Handling duplicate file names
  ```dart
  // generated codes
  static const AssetGenImage imagesProfileJpg = AssetGenImage('assets/images/profile.jpg'); 
  static const AssetGenImage imagesProfilePng = AssetGenImage('assets/images/profile.png');
  ```


**Bug fix**
- [#75](https://github.com/FlutterGen/flutter_gen/issues/75) Null safety support for generated files 

## 1.3.1

**Bug fix**
- [#60](https://github.com/FlutterGen/flutter_gen/issues/60) Set files like .DS_Store to the ignore list.

## 1.3.0

New Feature
- [#46](https://github.com/FlutterGen/flutter_gen/issues/46) Added support for unknown mime type files.
- Added support for [Rive (previously Flare)](https://rive.app/) files.

## 1.2.2

**Bug fix**
- [#51](https://github.com/FlutterGen/flutter_gen/pull/51) Added support for Key parameter in image() and svg().

## 1.2.1

**Bug fix**
- [#42](https://github.com/FlutterGen/flutter_gen/pull/42) Generated output folder name not being respected

## 1.2.0

New Feature
- [#40](https://github.com/FlutterGen/flutter_gen/pull/40) Support MaterialAccentColor

## 1.1.0

New Feature
  - [#33](https://github.com/FlutterGen/flutter_gen/pull/33) Support to generate flat hierarchy assets with field name style:
    - camel-case
    - snake-case
    - dot-delimiter (Default)

## 1.0.3

**Bug fix**
  - Insufficient params of flutter_svg [#32](https://github.com/FlutterGen/flutter_gen/pull/34)
## 1.0.2

**Bug fix**
  - Generate sorted statements [#27](https://github.com/FlutterGen/flutter_gen/pull/27)
  - Make Windows work properly [#28](https://github.com/FlutterGen/flutter_gen/pull/28) 

## 1.0.1

**Bug fix**
  - Issue [#21](https://github.com/FlutterGen/flutter_gen/issues/21)

## 1.0.0

Initial release.

- Assets generator
  - Supported image type.
  - Supported SVG as an integration.
  - And others.

- Fonts generator
- Colors generator
  - Supported xml file.
    - MaterialColor
