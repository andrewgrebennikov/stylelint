---
layout: page
title: # block-closing-brace-space-after
permalink: docs/src/rules/block-closing-brace-space-after/README/
---

# block-closing-brace-space-after

Require a single space or disallow whitespace after the closing brace of blocks.

```css
    a { color: pink; }
/**                  ↑
 * The space after this brace */
```

## Options

`string`: `"always"|"never"|"always-single-line"|"never-single-line"|"always-multi-line"|"never-multi-line"`

### `"always"`

There *must always* be a single space after the closing brace.

The following patterns are considered warnings:

```css
a { color: pink; }b { color: red; }
```

```css
a { color: pink; }
b { color: red; }
```

The following patterns are *not* considered warnings:

```css
a { color: pink; } b { color: red; }
```

### `"never"`

There *must never* be whitespace after the closing brace.

The following patterns are considered warnings:

```css
a { color: pink; } b { color: red; }
```

```css
a { color: pink; }
b { color: red; }
```

The following patterns are *not* considered warnings:

```css
a { color: pink; }b { color: red; }
```

```css
a { color: pink;
}b { color: red; }
```

### `"always-single-line"`

There *must always* be a single space after the closing brace in single-line blocks.

The following patterns are considered warnings:

```css
a { color: pink; }b { color: red; }
```

The following patterns are *not* considered warnings:

```css
a { color: pink; } b { color: red; }
```

```css
a { color: pink;
}b { color: red; }
```

### `"never-single-line"`

There *must never* be whitespace after the closing brace in single-line blocks.

The following patterns are considered warnings:

```css
a { color: pink; } b { color: red; }
```

The following patterns are *not* considered warnings:

```css
a { color: pink; }b { color: red; }
```

```css
a { color: pink;
} b { color: red; }
```

### `"always-multi-line"`

There *must always* be a single space after the closing brace in multi-line blocks.

The following patterns are considered warnings:

```css
a { color: pink;
}b { color: red; }
```

The following patterns are *not* considered warnings:

```css
a { color: pink; }b { color: red; }
```

```css
a { color: pink;
} b { color: red; }
```

### `"never-multi-line"`

There *must never* be whitespace after the closing brace in multi-line blocks.

The following patterns are considered warnings:

```css
a { color: pink;
} b { color: red; }
```

The following patterns are *not* considered warnings:

```css
a { color: pink; } b { color: red; }
```

```css
a { color: pink;
}b { color: red; }
```