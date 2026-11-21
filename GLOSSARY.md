# gomic

Mesa de som para voz no Windows: a voz do microfone passa por uma cadeia de módulos, ajustada por calibração e por ajustes manuais, e chega a outros apps por um cabo virtual. Cada termo traz entre parênteses o nome usado no código, que é em inglês.

## Processamento

**Cadeia** (`chain`):
A sequência fixa de módulos por onde a voz passa: ganho de entrada, passa-alta, supressão de ruído, noise gate, EQ paramétrico, de-esser, compressor e limiter.
_Evitar_: pipeline, rack, cadeia de filtros

**Módulo** (`module`):
Uma etapa da cadeia, com liga/desliga, parâmetros e medidor próprios.
_Evitar_: filtro, efeito, plugin

**Supressão de ruído** (`noise suppression`):
O módulo que remove ruído da voz usando um modelo de IA.
_Evitar_: denoise, redução de ruído

**Modo de supressão** (`suppression mode`):
A escolha entre modo Qualidade e modo Baixa latência para a supressão de ruído.
_Evitar_: "modo" sozinho, nível de supressão

**Modo Qualidade** (`quality`):
O modo de supressão que prioriza a voz mais limpa, aceitando mais latência.
_Evitar_: modo HQ, modo normal

**Modo Baixa latência** (`low latency`):
O modo de supressão que prioriza o menor atraso, com supressão leve ou desligada.
_Evitar_: modo rápido, modo leve

**Original** (`original`):
O áudio do microfone antes da cadeia.
_Evitar_: cru, bruto, dry

**Processado** (`processed`):
O áudio depois de passar pela cadeia.
_Evitar_: tratado, wet

## Medição e calibração

**Medição** (`measurement`):
Um valor calculado sobre o áudio: pico, nível, loudness, ruído de fundo, energia por faixa ou sibilância.
_Evitar_: métrica, leitura

**Medidor** (`meter`):
A exibição ao vivo das medições de um módulo ou da saída da cadeia.
_Evitar_: VU, indicador

**Ruído de fundo** (`noise floor`):
O nível do áudio quando ninguém está falando, em dB.
_Evitar_: chiado, ruído ambiente

**Sibilância** (`sibilance`):
Energia excessiva na faixa de 5 a 9 kHz, típica dos "s" estridentes.

**Calibração** (`calibration`):
A análise de um trecho de voz seguido de silêncio que gera parâmetros para o perfil por regras fixas, sem LLM. Acontece só quando pedida, nunca de forma contínua.
_Evitar_: auto-ajuste, otimização, autotune

**Relatório de calibração** (`calibration report`):
As medições que a calibração obteve, mostradas ao usuário junto com os parâmetros gerados.
_Evitar_: diagnóstico, análise

**Ajuste manual** (`manual override`):
Um valor de parâmetro definido pelo usuário, que prevalece sobre a calibração até ser desfeito, parâmetro por parâmetro ou todos de uma vez.
_Evitar_: override, customização

**A/B** (`a/b`):
Alternar entre ouvir o original e o processado, vendo as medições de cada um.
_Evitar_: bypass, comparação

## Configuração e dispositivos

**Perfil** (`profile`):
Um conjunto com nome de parâmetros da calibração, ajustes manuais e modo de supressão, salvo em arquivo local. Lembra o nome do microfone usado na calibração, para sugerir recalibrar quando o microfone muda.
_Evitar_: preset, configuração, cena

**Microfone** (`input device`):
O dispositivo de entrada escolhido, conhecido só pelo nome que o Windows informa. O gomic nunca identifica marca nem modelo.
_Evitar_: identificação do microfone, modelo do microfone

**Cabo virtual** (`virtual cable`):
O dispositivo de áudio virtual (VB-CABLE) por onde o processado chega a outros apps, que o escolhem como microfone.
_Evitar_: saída virtual, driver

**Monitoramento** (`monitoring`):
Ouvir o processado no próprio fone enquanto se fala.
_Evitar_: retorno, sidetone

## Interface

**Modo da interface** (`ui mode`):
A escolha entre modo simples e modo avançado.
_Evitar_: "modo" sozinho, vista

**Modo simples** (`simple`):
O modo da interface com poucos controles: liga/desliga geral, Calibrar, A/B, perfil e medidor.
_Evitar_: modo básico, modo fácil

**Modo avançado** (`advanced`):
O modo da interface que mostra todos os módulos da cadeia com seus controles e medidores.
_Evitar_: mesa completa, modo expert

## Casos de uso

**Tempo real** (`realtime`):
O caso de uso em que o processado vai para outros apps enquanto a pessoa fala (calls, Discord, lives).
_Evitar_: ao vivo, streaming

**Gravação** (`recording`):
O caso de uso futuro em que o processado é salvo em arquivo com a mesma cadeia.

**Caso de uso músico** (`musician`):
O caso de uso futuro com latência muito baixa e sem supressão agressiva.
_Evitar_: modo músico
