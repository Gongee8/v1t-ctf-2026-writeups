# 🦆 Curl the Duck

## Challenge Information

| Item | Value |
|------|-------|
| Category | Duck |
| Challenge | Curl the Duck |
| Points | 18 |

---

## Description

> Just .... `curl v1t.site/duck`

---

## Objective

Retrieve the hidden flag using the `curl` command-line tool.

---

## Solution

### Step 1 - Read the Challenge Hint

The challenge explicitly suggested using `curl` instead of accessing the website through a browser.

```bash
curl https://v1t.site/duck
```

The response displayed an ANSI-art interface instead of the flag.

It also listed several available endpoints:

```
curl v1t.site/ping
curl v1t.site/help
curl v1t.site/duck
curl v1t.site/flag
```

---

### Step 2 - Download the Flag File

Following the available commands, I requested the `/flag` endpoint and saved its output to a local file.

```bash
curl https://v1t.site/flag -o flag
```

The `-o` option tells `curl` to save the server response into a file instead of displaying it in the terminal.

---

### Step 3 - Inspect the Downloaded File

Verified that the file had been downloaded successfully.

```bash
ls
```

Output:

```
flag
```

---

### Step 4 - Display the File

Using the correct filename:

```bash
cat flag
```

displayed a large block-art image composed of Unicode characters.

---

### Step 5 - Render the Unicode Art

At first, the flag was difficult to read because the VirtualBox window was too small, causing the terminal to compress the Unicode block characters.

After maximizing the VirtualBox window (or enlarging the terminal), the Unicode art rendered correctly, revealing the hidden flag.

```
V1T{ducky_quacky}
```

---

## Flag

```text
V1T{ducky_quacky}
```

---



## Lessons Learned

- The `-o` option in `curl` is useful for saving server responses.
- Not every flag is returned as plain text; some are rendered as Unicode or ANSI art.
- Terminal size and font rendering can affect how Unicode graphics appear.
