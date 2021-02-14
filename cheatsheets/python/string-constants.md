# String constants

## Setup

```python
import string
```


## ASCII

```python
>>> string.ascii_lowercase
'abcdefghijklmnopqrstuvwxyz'
```

```python
>>> string.ascii_uppercase
'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
```

```python
>>> string.ascii_letters
'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'
```


## Numbers

```python
>>> string.digits
'0123456789'
```

Mix like this:

```python
>>> string.ascii_uppercase + string.digits
'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789'
```


## Punctuation

```python
>>> string.punctuation
'!"#$%&\'()*+,-./:;<=>?@[\\]^_`{|}~'
```


## Whitespace

```python
>>> string.whitespace
' \t\n\r\x0b\x0c'
```


## Printable

Numbers, ASCII, puncutation and whitespace.

```python
>>> string.printable
'0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ!"#$%&\'()*+,-./:;<=>?@[\\]^_`{|}~ \t\n\r\x0b\x0c'
```