# 🦆 Rules

## Challenge Information

- **Category:** Duck
- **Challenge:** Rules
- **Points:** 11

---

## Description

> Read the rule pretty please :(

---

## Objective

Find the hidden flag.

---

## Solution

Since all flags follow the V1T{...} format, I searched the page source for V1T{ using the browser's Find feature (Ctrl + F).
```
V1T{
```

5. Located the following HTML:

```html
<span class="troll-typing">
V1T{y3s_1_w1ll_0b3y_7h3_duck}
</span>
```

6. The HTML already contained the complete flag, but the CSS class .troll-typing prevented it from being displayed immediately by using:

- `overflow: hidden`
- `width: 0`
- a `typing` animation

to reveal the text slowly, making it appear as if someone is typing it. Viewing the page source bypasses this visual effect and exposes the full flag immediately.

## Lessons Learned

- Always inspect the page source during web challenges.
- CSS animations should not be considered a security mechanism.
- Hidden HTML content can often be discovered without executing JavaScript.
- Always inspect the page source during web challenges.
- CSS animations may hide or delay the display of sensitive information.
- Hidden content in HTML can often be discovered without interacting with JavaScript.
