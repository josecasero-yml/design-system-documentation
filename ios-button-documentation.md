**CLASS**

# `MayoButton`

```swift
open class MayoButton: UIButton
```

Button component for the Mayo Clinic design system

## Properties
### `isEnabled`

```swift
override open var isEnabled: Bool
```

A Boolean value indicating whether the `MayoButton` is in the enabled state.

### `isHighlighted`

```swift
override open var isHighlighted: Bool
```

A Boolean value indicating whether the `MayoButton` draws a highlight.

### `isSelected`

```swift
override open var isSelected: Bool
```

A Boolean value indicating whether `MayoButton` is in the selected state.

### `layout`

```swift
public private(set) var layout: TypographyLayout!
```

The current typographical layout

### `typography`

```swift
public var typography: Typography
```

Typography to be used for this buttons's title label

### `maximumPointSize`

```swift
public var maximumPointSize: CGFloat?
```

(Optional) maximum point size when scaling the font.

Value should be greater than Typography.fontSize.
`nil` means no maximum for scaling.
Has no effect for fixed Typography.

If you wish to set a specific maximum scale factor instead of a fixed maximum point size,
set `maximumScaleFactor` instead.
`maximumScaleFactor` will be used if both properties are non-nil.

### `maximumScaleFactor`

```swift
public var maximumScaleFactor: CGFloat?
```

(Optional) maximum scale factor to use when scaling the font.

Value should be greater than 1.
`nil` means no maximum scale factor.
Has no effect for fixed Typography.

If you wish to set a specific maximum point size instead of a scale factor, set `maximumPointSize` instead.
Takes precedence over `maximumPointSize` if both properties are non-nil.

### `paragraphStyle`

```swift
public var paragraphStyle: NSParagraphStyle
```

The paragraph style used to style this button's title label.
It combines the line height from the `Typography` with text alignment and line break mode.

### `textAlignment`

```swift
public var textAlignment: NSTextAlignment = .natural
```

Gets or sets the text alignment of the button's title label.
Default value = `.natural`

### `lineBreakMode`

```swift
public var lineBreakMode: NSLineBreakMode = .byTruncatingTail
```

Gets or sets the line break mode of the button's title label.
Default value = `.byTruncatingTail`

## Methods
### `init(typography:)`

```swift
required public init(typography: Typography)
```

Initializes a button using the specified `Typography`
- Parameter typography: the font information to use

#### Parameters

| Name | Description |
| ---- | ----------- |
| typography | the font information to use |

### `init(title:icon:)`

```swift
public convenience init(title: String, icon: UIImage)
```

Initializes a button with an icon in the leading position.
- Parameter icon: The image to use as the icon of the button.
- Parameter title: The title text to show in the button.

#### Parameters

| Name | Description |
| ---- | ----------- |
| icon | The image to use as the icon of the button. |
| title | The title text to show in the button. |

### `init(coder:)`

Required initializer for the Mayo button.
- Warning: Throws fatal error, do not use

### `layoutSubviews()`

```swift
override open func layoutSubviews()
```

Sets the corner radius to have rounded corners.

### `traitCollectionDidChange(_:)`

```swift
override open func traitCollectionDidChange(_ previousTraitCollection: UITraitCollection?)
```

Adjusts the fonts, colors and breakpoint of `MayoButton` when the iOS interface environment changes. Inherits from `UIButton`.
- Parameter previousTraitCollection: The UITraitCollection object before the interface environment changed.

#### Parameters

| Name | Description |
| ---- | ----------- |
| previousTraitCollection | The UITraitCollection object before the interface environment changed. |

### `adjustFonts()`

```swift
open func adjustFonts()
```

Called when when preferred content size or legibility weight has changed.

### `adjustColors()`

```swift
open func adjustColors()
```

Override this if you have colors that will not automatically adjust to
Light / Dark mode, etc. This can be the case for CGColor or
non-template images (or backgroundImages).

### `adjustBreakpoint()`

```swift
open func adjustBreakpoint()
```

Override this if you have typography that might change at different breakpoints.
You should check `.window?.bounds.size` for potential changes.

### `setTitle(_:for:)`

```swift
override public func setTitle(_ title: String?, for state: UIControl.State)
```

Set the title to use for the specified state. Overrides the `UIButton` default implementation.
- Parameters:
  - title: The title to use for the specified state.
  - state: The state that uses the specified title. `UIControl.State` describes the possible values.

#### Parameters

| Name | Description |
| ---- | ----------- |
| title | The title to use for the specified state. |
| state | The state that uses the specified title. `UIControl.State` describes the possible values. |

### `setAttributedTitle(_:for:)`

```swift
override public func setAttributedTitle(_ title: NSAttributedString?, for state: UIControl.State)
```

Sets the styled title to use for the specified state. Overrides the `UIButton` default implementation.
- Parameters:
  - title: The styled text string so use for the title.
  - state: The state that uses the specified title. The possible values are described in `UIControl.State`.

#### Parameters

| Name | Description |
| ---- | ----------- |
| title | The styled text string so use for the title. |
| state | The state that uses the specified title. The possible values are described in `UIControl.State`. |
