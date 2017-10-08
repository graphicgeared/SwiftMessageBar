[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![Version](https://img.shields.io/cocoapods/v/SwiftMessageBar.svg?style=flat)](http://cocoapods.org/pods/SwiftMessageBar)
[![License](https://img.shields.io/cocoapods/l/SwiftMessageBar.svg?style=flat)](http://cocoapods.org/pods/SwiftMessageBar)
[![Platform](https://img.shields.io/cocoapods/p/SwiftMessageBar.svg?style=flat)](http://cocoapods.org/pods/SwiftMessageBar)

# SwiftMessageBar

An iOS message bar, written in Swift

![image](https://www.dropbox.com/s/m0vcdcor6hw4e7a/SwiftMessageBar-2016.06.08.gif?raw=1)

## Requirements

- iOS 9.3+
- Swift 4
- Xcode 9+ 

## Installation

You can use [Carthage](https://github.com/Carthage/Carthage):

```ogdl
github "JanGorman/SwiftMessageBar"
```

or [CocoaPods](http://cocoapods.org):

```ruby
pod 'SwiftMessageBar'
```

## Usage

The included sample code shows how to use the message bar. There are three different message types:

```swift
enum MessageType {
    case Error, Success, Info
}
```

To display a message:

```swift
import SwiftMessageBar

@IBAction func showSuccess(sender: AnyObject) {
	SwiftMessageBar.showMessageWithTitle("Success", message: "The Message Body", type: .Success)
}
```

You can customize the duration of each message and also pass in a tap handler closure that is executed when a user taps on the message.

To customize the look of the messages, create a custom `MessageBarConfig` and set it on the shared messagebar. You can adjust colors, fonts as well as custom images. `MessageBarConfig` comes with a Builder class for easy configuration:

```swift
let config = MessageBarConfig.Builder()
```

## Licence

Agrume is released under the MIT license. See LICENSE for details



