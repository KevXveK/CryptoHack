# Notes

## Level 0 — Morse

Não é desafio oficial, só um aquecimento antes de entrar na categoria General de verdade. Serviu pra perceber que toda codificação "simples" é um dicionário de mão única.

## Level 1 — ASCII

Lista de números, `chr()` em cada um. Mesma lógica do morse, só que com uma tabela que eu não precisei inventar.

## Level 2 — Hex

`bytes.fromhex()` resolve sozinho. Mais direto que os dois anteriores porque não precisei escrever nenhum dicionário.

## Level 3 — Hex → Base64

Esse não decodifica pra texto legível de propósito, é só treino de `base64.b64encode()`. O resultado saiu formando uma frase por coincidência do alfabeto do base64 — não é flag, só uma curiosidade.

## Level 4 — Bytes and Big Integers

O que mais me confundiu no começo: um inteiro gigante é só o texto lido como número em base 10. Ajudou fazer o caminho de volta com uma palavra simples ("HELLO") antes de confiar no resultado com a flag de verdade.

## Status

- [x] Level 0 — Morse
- [x] Level 1 — ASCII
- [x] Level 2 — Hex
- [x] Level 3 — Hex → Base64 (treino)
- [x] Level 4 — Bytes and Big Integers
