# Notes

## Level 0 — Morse

Not an official challenge, just a warm-up before getting into the real General category. Good reminder that every "simple" encoding is basically a one-way dictionary.

## Level 1 — ASCII

A list of numbers, `chr()` on each one. Same idea as Morse, just with a table I didn't have to invent myself.

## Level 2 — Hex

`bytes.fromhex()` handles it on its own. More direct than the previous two since there's no dictionary to write.

## Level 3 — Hex → Base64

Doesn't decode into readable text on purpose — just a drill for `base64.b64encode()`. The output happened to spell out a readable phrase by coincidence of the base64 alphabet — not a flag, just a fun side effect.

## Level 4 — Bytes and Big Integers

The part that confused me most at first: a giant integer is just the text read as a base-10 number. Working backward with a simple word ("HELLO") first helped before trusting the result on the real flag.

## Status

- [x] Level 0 — Morse
- [x] Level 1 — ASCII
- [x] Level 2 — Hex
- [x] Level 3 — Hex → Base64 (drill)
- [x] Level 4 — Bytes and Big Integers
