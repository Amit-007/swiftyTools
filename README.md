**SwiftyTools**:

---

# SwiftyTools

[![Swift Version](https://img.shields.io/badge/Swift-5.0%2B-orange.svg)](https://swift.org)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)]()
[![Coverage Status](https://img.shields.io/badge/coverage-100%25-brightgreen.svg)]()

SwiftyTools is a comprehensive utility library written in Swift, designed to simplify and enhance your Swift development experience. With a wide range of utility functions and extensions, SwiftyTools is the perfect companion for any Swift project. Plus, it's fully covered with unit tests, ensuring reliability and robustness.

## Features

- **String Extensions**: Convenient methods for string manipulation and validation.
- **Array Utilities**: Helpful functions for handling arrays, sorting, filtering, and more.
- **Date & Time Helpers**: Simplified date manipulation, formatting, and comparison.
- **Network Utilities**: Easy-to-use networking functions for making HTTP requests and handling responses.
- **File Management**: Efficient tools for reading, writing, and managing files.
- **JSON Handling**: Simple and safe JSON parsing and serialization.
- **Custom Operators**: Powerful and readable custom operators for common tasks.
- **100% Unit Test Coverage**: Every utility function is covered with unit tests to ensure the highest level of reliability.

## Installation

### Swift Package Manager

You can install SwiftyTools via [Swift Package Manager](https://swift.org/package-manager/) by adding the following line to your `Package.swift` file:

```swift
dependencies: [
    .package(url: "https://github.com/YourUsername/SwiftyTools.git", from: "1.0.0")
]
```

Then import SwiftyTools wherever you need it:

```swift
import SwiftyTools
```

### CocoaPods

To integrate SwiftyTools into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
pod 'SwiftyTools', '~> 1.0'
```

Then run:

```bash
pod install
```

## Usage

Here's a quick overview of what you can do with SwiftyTools:

### String Extensions

```swift
import SwiftyTools

let email = "test@example.com"
if email.isValidEmail {
    print("This is a valid email.")
}

let reversed = "Hello".reversedString // "olleH"
```

### Array Utilities

```swift
let numbers = [1, 2, 3, 4, 5]
let doubled = numbers.map { $0 * 2 } // [2, 4, 6, 8, 10]
```

### Date & Time Helpers

```swift
let now = Date()
let formatted = now.toString(format: "yyyy-MM-dd")
```

### Network Utilities

```swift
NetworkManager.shared.get(url: "https://api.example.com/data") { result in
    switch result {
    case .success(let data):
        print("Data received: \(data)")
    case .failure(let error):
        print("Error: \(error)")
    }
}
```

### File Management

```swift
let filePath = "/path/to/file.txt"
if FileHelper.fileExists(atPath: filePath) {
    let contents = try? FileHelper.readFile(atPath: filePath)
    print(contents)
}
```

## Unit Tests

SwiftyTools prides itself on being 100% unit test covered. To run the tests, simply use:

```bash
swift test
```

## Contributing

Contributions are welcome! Please fork the repository, make your changes, and submit a pull request. Make sure your code is well-tested to maintain our 100% coverage.

## License

SwiftyTools is released under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Feel free to modify this as needed!
