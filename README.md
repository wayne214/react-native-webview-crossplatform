# React Native WebView - a Modern, Cross-Platform WebView for React Native

### now,we can use the https://github.com/react-native-community/react-native-webview ，it support the method onShouldStartLoadWithRequest for Ios and Android

## Platforms Supported

- [x] iOS (both UIWebView and WKWebView)
- [x] Android

## Getting Started

```
$ yarn add react-native-webview-crossplatform
$ react-native link react-native-webview-crossplatform
```

## Usage

Import the `WebView` component from `react-native-webview-crossplatform` and use it like so:

```jsx
import React, { Component } from 'react';
import { StyleSheet, Text, View } from 'react-native';
import { WebView } from 'react-native-webview-crossplatform';

// ...
class MyWebComponent extends Component {
  render() {
    return (
      <WebView
        source={{ uri: 'https://infinite.red/react-native' }}
        style={{ marginTop: 20 }}
        onLoadProgress={e=>console.log(e.nativeEvent.progress)}
        onShouldStartLoadWithRequest={e=>{
        console.log(e.nativeEvent.progress)
        return true
        }}
      />
    );
  }
}
```

For more, read the [API Reference](./docs/Reference.md) and [Guide](./docs/Guide.md).

## License

MIT
