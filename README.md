Zeal
====

[![Swift 2.2](https://img.shields.io/badge/Swift-2.2-orange.svg?style=flat)](https://developer.apple.com/swift/)
[![Platforms OS X | Linux](https://img.shields.io/badge/Platforms-OS%20X%20%7C%20Linux-lightgray.svg?style=flat)](https://developer.apple.com/swift/)
[![License MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](https://tldrlegal.com/license/mit-license)
[![Slack Status](https://zewo-slackin.herokuapp.com/badge.svg)](https://zewo-slackin.herokuapp.com)

This fork of **Zeal** is a Venice-based HTTP client for **Swift 2**.

## Features

- [x] No `Foundation` dependency (**Linux ready**)

## Dependencies

**Zeal** is made of:

- [Venice](https://github.com/Zewo/Venice)
- [Core](https://github.com/Zewo/Core)
- [HTTP](https://github.com/Zewo/HTTP)
- [HTTPParser](https://github.com/Zewo/HTTPParser)

## Usage

```swift
import URI
import HTTP
import Zeal

let client = HTTPClient(host: "www.apple.com", port: 80)

client.get("/") { result in
    do {
        let response = try result()
        // do your thing! (:
    } catch {
        // something bad happened :(
    }
}
```

There's an example target called ZealTarget you can run after you `swift build` in the root of this repo.

## Installation

### SwiftPM

```swift
let package = Package(
    name: "YourProject",
    dependencies: [
        .Package(url: "https://github.com/Zewo/Venice.git", majorVersion: 0, minor: 1),
    ]
)
```

## Community

[![Slack](http://s13.postimg.org/ybwy92ktf/Slack.png)](https://zewo-slackin.herokuapp.com)

Join us on [Slack](https://zewo-slackin.herokuapp.com).

License
-------

**Zeal** is released under the MIT license. See LICENSE for details.
