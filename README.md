# React Native Github Markdown

Generate GitHub Flavored Markdown (with syntax highlight) using React Native WebView.

Screenshot 📱 👇

<img src="./screenshots/md-preview.jpg" width="400">

## Features

- Render GitHub Flavored Markdown on your React Native WebView.

- Auto-height WebView adjusted to the document.

- Code syntax highlighting.

- Dark mode!

## Install

```shell
npm i react-native-github-markdown
```

or

```shell
yarn add react-native-github-markdown
```

Your React Native configuration should [support](https://github.com/react-native-community/react-native-webview#platforms-supported) [`react-native-webview`](https://github.com/react-native-community/react-native-webview).

## Usage

```jsx
import MarkdownWebView from 'react-native-github-markdown';

<MarkdownWebView
  style={{marginTop: 10}}
  content={'# React Native Github Markdown\n\nHello world!'}
  highlight
  darkMode
/>;
```

## Props

- `defaultHeight`: default height when the actual height has not been computed.
- `content`: raw markdown content to render.
- `highlight`: whether to use `highlight.js` for syntax highlighting.
- `darkMode`: whether to set rendered results in dark mode.

---

- `WebViewProps`: same as [`react-native-webview`'s](https://github.com/react-native-community/react-native-webview/blob/master/docs/Reference.md).

## Caveats

- Code syntax highlighting seems odd for long code snippets. It's a problem with `highlight.js`. You can choose to disable it using the `highlight` prop.

## Behind the Scene

- Markdown generated by [marked](https://github.com/markedjs/marked) and use [DOMPurify](https://github.com/cure53/DOMPurify) for sanitizing.

- Syntax highlighted by [highlight.js](https://github.com/highlightjs/highlight.js).

- CSS from GitHub's [Primer](https://github.com/primer/css) and `highlight.js`.

- Dark mode applied by [darkreader](https://github.com/darkreader/darkreader).
