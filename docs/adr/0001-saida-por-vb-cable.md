# Saída para outros apps pelo VB-CABLE, instalado pelo usuário

O processado chega a outros apps por um cabo virtual pronto, o VB-CABLE, e não por um APO, um driver próprio ou um cabo virtual próprio: escrever e assinar um driver de áudio no Windows custaria mais que o resto do projeto. O gomic não embute o VB-CABLE no instalador. Ele trata o VB-CABLE como pré-requisito, detecta quando falta e orienta a instalação pelo site oficial.

## Considered Options

- **Embutir o VB-CABLE no instalador.** A licença da VB-Audio permite distribuir o pacote "AS IS" junto com outro app, mas exige identificar o VB-CABLE como produto da VB-Audio e donationware, e cobra licenças quando o app vai para empresas ou instituições. A própria VB-Audio indica o pré-requisito como o caminho mais simples. Rejeitado para não carregar essas obrigações.
- **APO ou driver próprio.** Rejeitado pela complexidade e pela assinatura de driver.

## Consequences

- Sem o VB-CABLE instalado, o tempo real não funciona; o aviso de ausência precisa ser claro.
- O VB-CABLE é donationware: uso pessoal é livre, uso profissional exige licença da VB-Audio. Isso vale para o usuário, não para o código do gomic.
- Fonte: https://vb-audio.com/Services/licensing.htm, consultada em 2026-11-21.
