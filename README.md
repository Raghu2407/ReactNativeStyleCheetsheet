# ⚛️ React Native Style Cheatsheet

> A complete, searchable reference for all React Native style properties — covering **Android & iOS** with platform-specific notes.

![React Native](https://img.shields.io/badge/React%20Native-0.73+-61DAFB?style=flat-square&logo=react&logoColor=black)
![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS-lightgrey?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## 📖 Overview

This cheatsheet covers **100+ style properties** across **12 categories**, built as an interactive React component. Useful as a quick reference while building React Native apps — no more digging through docs.

**Live Preview**: Drop `rn-style-cheatsheet.jsx` into any React environment (CodeSandbox, StackBlitz, your own project) to get an interactive, searchable UI.

---

## 📦 Categories Covered

| # | Category | Description |
|---|----------|-------------|
| 1 | **Layout & Flexbox** | `flex`, `flexDirection`, `justifyContent`, `alignItems`, `alignSelf`, `flexWrap`, and more |
| 2 | **Dimensions & Spacing** | `width`, `height`, `margin`, `padding` and all shorthand/directional variants |
| 3 | **Position** | `position`, `top`, `bottom`, `left`, `right`, `zIndex`, `overflow` |
| 4 | **Background & Colors** | `backgroundColor`, `opacity` |
| 5 | **Borders** | `borderWidth`, `borderRadius`, `borderColor`, `borderStyle` and per-side variants |
| 6 | **Typography** | `fontSize`, `fontWeight`, `fontFamily`, `textAlign`, `lineHeight`, `letterSpacing`, `textTransform`, and more |
| 7 | **Shadow & Elevation** | `elevation` (Android) · `shadowColor`, `shadowOffset`, `shadowOpacity`, `shadowRadius` (iOS) |
| 8 | **Image** | `resizeMode`, `tintColor`, `overlayColor` |
| 9 | **Transform** | `translateX/Y`, `scale`, `rotate`, `skewX/Y`, `perspective` |
| 10 | **Display & Visibility** | `display`, `backfaceVisibility`, `pointerEvents` |
| 11 | **Aspect Ratio** | `aspectRatio` |
| 12 | **ScrollView / List** | `contentContainerStyle`, `horizontal`, scroll indicators |

---

## 🚀 Usage

### Option 1 — Use the interactive JSX component

```bash
# Clone the repo
git clone https://github.com/your-username/rn-style-cheatsheet.git
cd rn-style-cheatsheet
```

Drop `rn-style-cheatsheet.jsx` into any React project:

```jsx
import Cheatsheet from './rn-style-cheatsheet';

export default function App() {
  return <Cheatsheet />;
}
```

### Option 2 — Use it as a reference below

Scroll down for the full property list.

---

## 🧩 Style Categories Quick Reference

### 1. Layout & Flexbox

```js
{
  flex: 1,
  flexDirection: 'row',          // 'row' | 'column' | 'row-reverse' | 'column-reverse'
  flexWrap: 'wrap',              // 'wrap' | 'nowrap' | 'wrap-reverse'
  justifyContent: 'center',     // 'flex-start' | 'flex-end' | 'center' | 'space-between' | 'space-around' | 'space-evenly'
  alignItems: 'stretch',        // 'flex-start' | 'flex-end' | 'center' | 'stretch' | 'baseline'
  alignSelf: 'auto',            // 'auto' | 'flex-start' | 'flex-end' | 'center' | 'stretch'
  alignContent: 'flex-start',   // multi-line cross-axis alignment
  flexGrow: 1,
  flexShrink: 0,
  flexBasis: 'auto',            // number | 'auto' | '%'
}
```

---

### 2. Dimensions & Spacing

```js
{
  width: 100,          // number | '%' | 'auto'
  height: 200,
  minWidth: 50,
  maxWidth: 400,
  minHeight: 50,
  maxHeight: 600,

  margin: 10,
  marginTop: 10,
  marginBottom: 10,
  marginLeft: 10,
  marginRight: 10,
  marginHorizontal: 10,   // left + right
  marginVertical: 10,     // top + bottom

  padding: 10,
  paddingTop: 10,
  paddingBottom: 10,
  paddingLeft: 10,
  paddingRight: 10,
  paddingHorizontal: 10,
  paddingVertical: 10,
}
```

---

### 3. Position

```js
{
  position: 'absolute',   // 'absolute' | 'relative' (default)
  top: 0,
  bottom: 0,
  left: 0,
  right: 0,
  zIndex: 10,
  overflow: 'hidden',     // 'visible' | 'hidden' | 'scroll' (iOS only for scroll)
}
```

---

### 4. Background & Colors

```js
{
  backgroundColor: '#fff',   // hex | rgba | named color
  opacity: 0.8,              // 0.0 – 1.0 (affects entire component + children)
}
```

---

### 5. Borders

```js
{
  borderWidth: 1,
  borderTopWidth: 1,
  borderBottomWidth: 1,
  borderLeftWidth: 1,
  borderRightWidth: 1,

  borderColor: '#ccc',
  borderTopColor: '#ccc',
  borderBottomColor: '#ccc',
  borderLeftColor: '#ccc',
  borderRightColor: '#ccc',

  borderRadius: 8,
  borderTopLeftRadius: 8,
  borderTopRightRadius: 8,
  borderBottomLeftRadius: 8,
  borderBottomRightRadius: 8,

  borderStyle: 'solid',     // 'solid' | 'dotted' | 'dashed'
}
```

---

### 6. Typography (Text only)

```js
{
  fontSize: 16,
  fontWeight: 'bold',           // 'normal' | 'bold' | '100' – '900'
  fontFamily: 'Roboto',
  fontStyle: 'italic',          // 'normal' | 'italic'
  color: '#333',

  textAlign: 'center',          // 'auto' | 'left' | 'right' | 'center' | 'justify'
  textAlignVertical: 'center',  // Android only — 'auto' | 'top' | 'bottom' | 'center'
  lineHeight: 24,
  letterSpacing: 0.5,

  textDecorationLine: 'underline',     // 'none' | 'underline' | 'line-through' | 'underline line-through'
  textDecorationStyle: 'solid',        // iOS only — 'solid' | 'double' | 'dotted' | 'dashed'
  textDecorationColor: 'red',          // iOS only

  textTransform: 'uppercase',   // 'none' | 'uppercase' | 'lowercase' | 'capitalize'

  textShadowColor: 'rgba(0,0,0,0.3)',
  textShadowOffset: { width: 1, height: 1 },
  textShadowRadius: 2,

  includeFontPadding: false,    // Android only — default true
  numberOfLines: 2,             // Truncate text
  ellipsizeMode: 'tail',        // 'head' | 'middle' | 'tail' | 'clip'
  writingDirection: 'ltr',      // iOS only — 'auto' | 'ltr' | 'rtl'
}
```

---

### 7. Shadow & Elevation

```js
// Android
{
  elevation: 5,   // Adds shadow on Android
}

// iOS
{
  shadowColor: '#000',
  shadowOffset: { width: 0, height: 2 },
  shadowOpacity: 0.25,
  shadowRadius: 4,
}
```

> **Tip:** Use a library like [`react-native-shadow-2`](https://github.com/SrBrahma/react-native-shadow-2) for cross-platform shadows.

---

### 8. Image

```js
{
  resizeMode: 'cover',       // 'cover' | 'contain' | 'stretch' | 'repeat' | 'center'
  tintColor: '#ff0000',      // Colorize the image
  overlayColor: '#fff',      // Android only — used with borderRadius on images
}
```

---

### 9. Transform

```js
{
  transform: [
    { translateX: 10 },
    { translateY: 20 },
    { scale: 1.5 },
    { scaleX: 1.2 },
    { scaleY: 0.8 },
    { rotate: '45deg' },
    { rotateX: '30deg' },
    { rotateY: '45deg' },
    { rotateZ: '90deg' },
    { skewX: '15deg' },
    { skewY: '10deg' },
    { perspective: 1000 },  // iOS only
  ],
}
```

---

### 10. Display & Visibility

```js
{
  display: 'flex',               // 'flex' | 'none' — 'none' hides & removes from layout
  backfaceVisibility: 'hidden',  // 'visible' | 'hidden'
  pointerEvents: 'auto',         // 'box-none' | 'none' | 'box-only' | 'auto'
}
```

---

### 11. Aspect Ratio

```js
{
  aspectRatio: 16 / 9,   // Maintains width/height ratio — e.g., 1 = square, 4/3, 16/9
}
```

---

### 12. ScrollView / List

```js
// On ScrollView
<ScrollView
  contentContainerStyle={{ padding: 16 }}
  horizontal={false}
  showsVerticalScrollIndicator={false}
  showsHorizontalScrollIndicator={false}
/>
```

---

## 🏷️ Platform Indicators

| Badge | Meaning |
|-------|---------|
| `[Android]` | Property only works on Android |
| `[iOS]` | Property only works on iOS |
| *(no badge)* | Works on both platforms |

---

## 📐 Units

| Unit | Platform | Description |
|------|----------|-------------|
| `dp` (density-independent pixels) | Android | Default numeric unit |
| `pt` (points) | iOS | Default numeric unit |
| `%` | Both | Percentage of parent |
| `'auto'` | Both | Computed by layout engine |

> React Native uses unitless numbers — you don't write `px`. On Android this maps to `dp`, on iOS to `pt`.

---

## 🔗 Resources

- [Official RN Style Docs](https://reactnative.dev/docs/style)
- [View Style Props](https://reactnative.dev/docs/view-style-props)
- [Text Style Props](https://reactnative.dev/docs/text-style-props)
- [Image Style Props](https://reactnative.dev/docs/image-style-props)
- [Layout with Flexbox](https://reactnative.dev/docs/flexbox)
- [StyleSheet API](https://reactnative.dev/docs/stylesheet)

---

## 🤝 Contributing

PRs welcome! If a property is missing or incorrect, feel free to open an issue or submit a pull request.

1. Fork the repo
2. Create your branch: `git checkout -b fix/missing-prop`
3. Commit your changes: `git commit -m 'Add missing prop'`
4. Push and open a PR

---

## 📄 License

MIT © [your-username](https://github.com/your-username)
