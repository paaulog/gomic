# Dois modos de supressão: DeepFilterNet e RNNoise

Não existe um supressor de ruído que seja ao mesmo tempo o mais limpo e o de menor atraso, então a supressão de ruído tem dois modos: modo Qualidade com DeepFilterNet (implementação nativa em Rust) e modo Baixa latência com RNNoise ou supressão desligada. As metas de latência (até 60 ms e até 20 ms no total) estão a confirmar pelo protótipo de latência.

## Licenças

Conferidas em 2026-11-21, ambas compatíveis com a licença MIT do gomic:

- **DeepFilterNet**: código e pesos do modelo sob MIT ou Apache-2.0, à escolha (https://github.com/Rikorose/DeepFilterNet).
- **RNNoise**: BSD-3-Clause (https://github.com/xiph/rnnoise).

Distribuir o gomic exige incluir os avisos de licença dos dois junto com o programa.
