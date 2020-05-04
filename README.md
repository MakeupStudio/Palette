<p align="center">
  <img src="Assets/Palette-Logo-Pink.png" width=100%/>
</p>

<p>    
  <a href="https://swift.org">
        <img src="https://img.shields.io/badge/Swift-5.1-red.svg?logo=swift" />
    </a>
    <a href="https://swift.org/package-manager">
        <img src="https://img.shields.io/badge/SwiftPM-Compatible-brightgreen.svg?style=flat" alt="SwiftPM" />
    </a>
    <img src="https://img.shields.io/badge/Platforms-Mac & Linux-green.svg?style=flat" alt="Mac & Linux" />
    <a href="https://twitter.com/maximkrouk">
        <img src="https://img.shields.io/badge/twitter-@maximkrouk-blue.svg?logo=twitter&style=social" alt="Twitter: @maximkrouk"/>
    </a>
</p>

Platform agnostic static factory of [colors](https://github.com/MakeupStudio/GenericColor).

## Usage

```swift
import Palette
```

```swift
let color1 = Color<RGB>.classicBlue // Pantone color of 2020
let color2 = Color<RGB>.livingCoral // Pantone color of 2019
print(color1 != color2) // true
```

Compatibility with NSColor/UIColor:

```swift
func setTextColor(_ color: Color<RGB>, to label: UILabel) {
    label.textColor = .init(color)
}

func getTextColor(from label: UILabel) -> Color<RGB> {
    return label.textColor.generic
}
```

See [RGBPalette](./Sources/Palette/RGBPalette.swift) for complete list of colors.

## Installation

**_See [this](https://github.com/MakeupStudio/Palette/tree/develop/4.0.0) for the latest version_**.

Add the package to Your SwiftPM package dependencies:

```swift
.package(
    url: "https://github.com/MakeupStudio/Palette.git", 
    .upToNextMajor(from: "3.0.0")
)
```

then add `Palette` dependency to your target.

## Licence

MIT
