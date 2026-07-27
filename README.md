# CryptoHack

Log pessoal de prática em [cryptohack.org](https://cryptohack.org). Uso isso como anotação e como um mini portfólio — write-ups curtos e honestos, não uma lista de flags só pra mostrar serviço.

## Níveis

| Nível | Desafio | Ideia central |
|-------|---------|----------------|
| [0](levels/level0.md) | Morse (aquecimento, não é oficial) | dicionário de codificação |
| [1](levels/level1.md) | ASCII → texto | `chr()` |
| [2](levels/level2.md) | Hex → texto | `bytes.fromhex()` |
| [3](levels/level3.md) | Hex → binário → Base64 (treino) | `base64.b64encode()` |
| [4](levels/level4.md) | Inteiro gigante → bytes | `hex()` + `bytes.fromhex()` |

## Estrutura

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

Ver [NOTES.md](NOTES.md) pras anotações de cada nível.

O repositório [OverTheWire](OverTheWire/README.md) que está ao lado é outro log separado (wargames de Linux/rede), guardado aqui só pelo estilo — não faz parte do CryptoHack.
