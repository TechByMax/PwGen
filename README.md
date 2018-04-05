# PwGen

[![Version](https://img.shields.io/cocoapods/v/PwGen.svg?style=flat)](http://cocoapods.org/pods/PwGen)
[![License](https://img.shields.io/cocoapods/l/PwGen.svg?style=flat)](http://cocoapods.org/pods/PwGen)
[![Platform](https://img.shields.io/cocoapods/p/PwGen.svg?style=flat)](http://cocoapods.org/pods/PwGen)

Simple yet cryptographically secure password generator library in Swift.

## Usage

### Generate password

Default password (12 characters) using symbols, letters and numbers:

```swift
let password: String = try! PwGen().generate()
```
Password of size 20 using only letters and numbers:

```swift
let password: String = try! PwGen().ofSize(20).withoutSymbols().generate()
```

Symbols, letters, numbers and added characters:

```swift
let password: String = try! PwGen().addCharacters(["€","£"]).generate()
```
Lowercase letters, numbers and symbols without the ! character:

```swift
let password: String = try! PwGen().withoutCharacter("!").withoutUppercase().generate()
```

### Check characters that will be used

```swift
let generator = PwGen().withoutSymbols()
print(generator.getCharacters())

let password: String = try! generator.generate()
```

## Installation

PwGen is available through [CocoaPods](http://cocoapods.org). 

To install it, simply add the following line to your Podfile:

```ruby
pod 'PwGen'
```

Then run:

```shell
pod install
```

## License

PwGen is available under the MIT license. See the LICENSE file for more info.
