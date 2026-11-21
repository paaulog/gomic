# gomic

Mesa de som para voz no Windows: melhora o áudio de qualquer microfone com uma cadeia de módulos, calibração automática e ajustes manuais, e entrega o resultado a outros apps pelo VB-CABLE. Não identifica marca nem modelo do microfone. A spec está na issue #1; o vocabulário fica em `GLOSSARY.md` e as decisões em `docs/adr/`.

Código (tipos, funções, testes) em inglês, usando o nome em inglês que o `GLOSSARY.md` dá para cada termo. Documentação, issues e conversa em português do Brasil.

## Processo

Este repo segue o fluxo das skills do Matt Pocock (plugin "Skills For Real Engineers", instalado na conta do Claude, não neste repo). Na dúvida sobre qual skill usar, rode `/ask-matt`.

Fluxo principal: `/grill-with-docs` → (`/prototype` se precisar ouvir/testar algo) → `/to-spec` → `/to-tickets` → `/implement` por ticket (com `/tdd` e `/code-review`) → `/retro`.

## Agent skills

### Issue tracker

Issues e specs vivem nas GitHub Issues deste repo, operadas pelo `gh` CLI. See `docs/agents/issue-tracker.md`.

### Triage labels

Labels padrão: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: um `GLOSSARY.md` e `docs/adr/` na raiz. See `docs/agents/domain.md`.
