# gomic

Software para identificar e melhorar qualquer microfone. O escopo ainda está sendo definido via `/grill-with-docs`; as decisões ficam em `CONTEXT.md` e `docs/adr/`.

## Processo

Este repo segue o fluxo das skills do Matt Pocock (plugin "Skills For Real Engineers", instalado na conta do Claude, não neste repo). Na dúvida sobre qual skill usar, rode `/ask-matt`.

Fluxo principal: `/grill-with-docs` → (`/prototype` se precisar ouvir/testar algo) → `/to-spec` → `/to-tickets` → `/implement` por ticket (com `/tdd` e `/code-review`) → `/retro`.

## Agent skills

### Issue tracker

Issues e specs vivem nas GitHub Issues deste repo, operadas pelo `gh` CLI. See `docs/agents/issue-tracker.md`.

### Triage labels

Labels padrão: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: um `CONTEXT.md` e `docs/adr/` na raiz. See `docs/agents/domain.md`.
