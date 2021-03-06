# function-whitespace-after

Require or disallow whitespace after functions.

```css
    a { transform: translate(1, 1) scale(3); }
/**                               ↑
 *                       This space */
```

The rule does not check for space immediately after `)` if the very next character
is `,`, `)`, or `}`, allowing some of the patterns exemplified below.

## Options

`string`: `"always"|"never"`

### `"always"`

There *must always* be whitespace after the function.

The following patterns are considered warnings:

```css
a { transform: translate(1, 1)scale(3); }
```

The following patterns are *not* considered warnings:

```css
a { transform: translate(1, 1) scale(3); }
```

```css
a { transform: translate(1, 1)     scale(3); }
```

```css
a {
  transform:
    translate(1, 1)
    scale(3);
}
```

```css
/* notice the two closing parentheses without a space between */
a { top: calc(1 * (1 + 3)); }
```

```css
/* notice the ), with no space after the closing parenthesis */
a { padding: calc(1 * 2px), calc(2 * 5px); }
```

```scss
/* notice the )}, with no space after the closing parenthesis */
h1 {
  max-height: #{($line-height) * ($lines-to-show)}em;
}
```scss

### `"never"`

There *must never* be whitespace after the function.

The following patterns are considered warnings:

```css
a { transform: translate(1, 1) scale(3); }
```

The following patterns are *not* considered warnings:

```css
a { transform: translate(1, 1)scale(3); }
```
