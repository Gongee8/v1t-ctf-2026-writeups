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

## Methodology

1. Opened the **Rules** challenge.

2. The page did not immediately display the flag.

3. Opened the page source (`Ctrl + U`).

4. Searched for the flag format:

```
V1T{
```

5. Located the following HTML:

```html
<span class="troll-typing">
V1T{y3s_1_w1ll_0b3y_7h3_duck}
</span>
```

6. The CSS class `.troll-typing` uses:

- `overflow: hidden`
- `width: 0`
- a `typing` animation

to reveal the text slowly, making it appear as if someone is typing it. Viewing the page source bypasses this visual effect and exposes the full flag immediately.
- Always inspect the page source during web challenges.
- CSS animations may hide or delay the display of sensitive information.
- Hidden content in HTML can often be discovered without interacting with JavaScript.
