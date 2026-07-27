# CryptoHack

Personal practice log for [cryptohack.org](https://cryptohack.org). Using this as notes and a small portfolio — short, honest write-ups, not just a list of flags to show off.

## Levels

| Level | Challenge | Core idea |
|-------|-----------|-----------|
| [0](levels/level0.md) | Morse (warm-up, not official) | encoding dictionary |
| [1](levels/level1.md) | ASCII → text | `chr()` |
| [2](levels/level2.md) | Hex → text | `bytes.fromhex()` |
| [3](levels/level3.md) | Hex → binary → Base64 (drill) | `base64.b64encode()` |
| [4](levels/level4.md) | Big integer → bytes | `hex()` + `bytes.fromhex()` |

## Structure

```
.
├── README.md
├── NOTES.md
└── levels/
    ├── level0.md
    ├── level1.md
    ├── level2.md
    ├── level3.md
    └── level4.md
```

See [NOTES.md](NOTES.md) for per-level notes.

The [OverTheWire](OverTheWire/README.md) folder next to this one is a separate log (Linux/network wargames), kept here just for the shared style — it isn't part of CryptoHack.
