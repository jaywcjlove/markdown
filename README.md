Markdown
===

[![CI](https://github.com/jaywcjlove/markdown/actions/workflows/ci.yml/badge.svg)](https://github.com/jaywcjlove/markdown/actions/workflows/ci.yml)
![SwiftUI Support](https://shields.io/badge/SwiftUI-macOS%20v10.15%20%7C%20iOS%20v13-green?logo=Swift&style=flat)

Render Markdown text in SwiftUI. It is a preview based on the [`Marked`](https://github.com/markedjs/marked) implementation.

![Markdown Package Screenshot](https://user-images.githubusercontent.com/1680273/157746319-d338670c-e4b2-471b-b524-0e9ecb8d2c52.png)

## Installation

You can add MarkdownUI to an Xcode project by adding it as a package dependency.

1. From the File menu, select Add Packages…
2. Enter https://github.com/jaywcjlove/markdown the Search or Enter Package URL search field
3. Link `Markdown` to your application target

Or add the following to `Package.swift`:

```swift
.package(url: "https://github.com/sindresorhus/is-camera-on", from: "1.0.0")
```

Or [add the package in Xcode](https://developer.apple.com/documentation/xcode/adding_package_dependencies_to_your_app).

## Usage

```swift
import SwiftUI
import Markdown

struct ContentView: View {
  @State private var mdStr: String = """
    ## Hello World
    
    Render Markdown text in SwiftUI.
    """
  var body: some View {
    VStack {
      Markdown(content: $mdStr)
      TextEditor(text: $mdStr)
    }
  }
}
```

## License

Licensed under the MIT License.
