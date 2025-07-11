
---

# Flex-Packages

## Flex Import System Overview

Flex supports a flexible import system that allows you to include external `.lx` or `.flex` files into your program. The language supports **three equivalent import keywords**:

* `geeb`
* `geep`
* `import`

All three serve the same purpose but reflect different syntax preferences to support Flex's bilingual design (Franco Arabic and English).

---

## Import Keywords Explained

### 1. `geeb` — Franco Arabic Import

Use `geeb` when writing in Franco Arabic style.

**Example:**

```flex
# File: math_utils.lx
sando2 absolute(rakm a){
    lw a < 0 {
        x = a * (-1)
        rg3 x
    }
    gher {
        rg3 a
    }
}
```

```flex
# File: main.lx
geeb "path/to/math_utils.lx"

x = -400
positive = absolute(x)
etb3("{x} after absolute is {positive}")
```

---

### 2. `geep` — Alternative Franco Arabic Import

`geep` functions exactly like `geeb` and is interchangeable.

**Example:**

```flex
# File: main.lx
geep "path/to/math_utils.lx"

x = -400
positive = absolute(x)
etb3("{x} after absolute is {positive}")
```

---

### 3. `import` — English Style Import

`import` is the English-style keyword, identical in functionality to `geeb` and `geep`.

**Example:**

```flex
# File: main.lx
import "path/to/math_utils.lx"

x = -400
positive = absolute(x)
etb3("{x} after absolute is {positive}")
```

---

## Parser Behavior

All three keywords (`geeb`, `geep`, `import`) are handled identically by the Flex parser. It looks for a string path following any of these keywords and loads the corresponding module.

---

## Practical Example

Example usage from a real test file:

```flex
geeb "C:/Users/hp/Desktop/Github/Flex/Flex/src/flex_tester"

fo()
r = tmsss(3, 9)
etb3(r)
```

---

## Notes

* All three keywords are **functionally identical**.
* Use `geeb` or `geep` for Franco Arabic syntax.
* Use `import` for standard English syntax.
* This import flexibility is part of Flex’s design to support bilingual code and developer preference.

---
