# Base64 encoding

- [Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)
- [Base32 on Wikipedia](https://en.wikipedia.org/wiki/Base32)


## Index table

Values 0 to 61 are the following, in order:

- `A` – `Z`
- `a` – `z`
- `0` – `9`

Then the last two values can change but typically `+` and `/`.

Padding character: `=`.

## Usage

### Browser JavaScript

Use the built-in functions `btoa` and `atob`. You can use these directly in the browser. But not in Node.

Note that `b` stands for [binary string](https://developer.mozilla.org/en-US/docs/Web/API/DOMString/Binary) (UTF-16 encoded strings) and **not** base-64.

From [Mozilla docs](https://developer.mozilla.org/en-US/docs/Glossary/Base64):

> In JavaScript there are two functions respectively for decoding and encoding base64 strings:
>
> - `btoa()`: creates a base-64 encoded ASCII string from a "string" of binary data ("btoa" should be read as "binary to ASCII").
> - `atob()`: decodes a base-64 encoded string ("atob" should be read as "ASCII to binary").

### Encode

Convert from binary string to base-64 ASCII string.

```javascript
> btoa("Hello, world!")
"SGVsbG8sIHdvcmxk"
```

### Decode

```javascript
> atob("SGVsbG8sIHdvcmxk")
"Hello, world!"
```

## Node

Using the built-in [buffer](https://nodejs.org/api/buffer.html) API. No imports are needed.

```javascript
const buf = Buffer.from('hello world', 'utf8');

buf.toString('hex')
// 68656c6c6f20776f726c64

buf.toString('base64')
//  aGVsbG8gd29ybGQ=
```


## Python

```python
>>> base64.b64decode('SGVsbG8sIHdvcmxkIQ==')
b'Hello, world!'
```

See [Python Base 64][] cheatsheet for more info.

[Python Base 64]: {% link cheatsheets/python/strings/encoding/base64.md %}

### Shell

- [base64](https://linux.die.net/man/1/base64) Linux man page.

Use `base64` and `-d` or `--decode` to decode.

Encode:

```sh
$ echo  'Hello, world!' | base64
SGVsbG8sIHdvcmxkIQo=
```

Decode:

```sh
$ echo 'SGVsbG8sIHdvcmxkIQo=' | base64 -d
Hello, world!
```
