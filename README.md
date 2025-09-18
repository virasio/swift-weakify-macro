# Swift Weakify Macro

🚧 **Work in Progress** - Learning project for Swift macro development

## Overview

This repository documents my journey learning Swift macros by implementing a `#weakify` macro for safe weak reference capture in closures.

## Goal

Create a macro that transforms:

```swift
someClosure = #weakify {
    self.doSomething()
}
```

Into safe weak reference capture:

```swift
someClosure = { [weak self] in
    guard let self = self else { return }
    self.doSomething()
}
```

## Learning Plan

- [ ] Implement basic macro structure
- [ ] Add closure transformation logic
- [ ] Write comprehensive tests
- [ ] Document findings and challenges
- [ ] Explore Swift macro system fundamentals
- [ ] Study `swift-syntax` package and AST manipulation

## Resources

- [Swift Macros Documentation](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/macros/)
- [swift-syntax Package](https://github.com/apple/swift-syntax)
- [WWDC 2023: Write Swift Macros](https://developer.apple.com/videos/play/wwdc2023/10166/)

## Requirements

- Swift 6.2+
- Xcode 26.0+

---

Follow along as I learn Swift macros step by step! 📚
