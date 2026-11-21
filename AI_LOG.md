# Registro de uso de IA da equipe

O código inicial fornecido pelo docente é identificado pelo primeiro commit.
Registre abaixo o uso de IA nas alterações da equipe; se não houve, registre isso.

| Data e ferramenta | Pedido | Aceito | Rejeitado | Justificativa técnica e validação |
|---|---|---|---|---|
| 2026-11-16 · Antigravity (Gemini) | Leitura do edital (`especificacao-projeto-final.pdf`), análise do starter (`poo-planta-controle`), comparação de cenários de automação, políticas de controle e padrões de projeto com trade-offs e diagramas Mermaid em `docs/ARQUITETURA_E_DECISOES.md`. | Cenário do Fermentador Cervejeiro (preservando tags `LT-01`, `TT-01`, `bomba`, `aquecedor`), `PoliticaHisterese` (principal) + `PoliticaProporcional` (segunda estratégia obrigatória) e padrões `Strategy`, `Command` e `Repository`. | Cenários que alteravam unidades ou sinal físico da planta (ex.: Chiller de Data Center e Cloração em mg/L) e uso de `Observer` como padrão primário no processo síncrono `--uma-vez`. | Mantém 100% de compatibilidade com os contratos de `tests/test_controlador.py` e `tests/test_supervisor.py` e evita notificações duplicadas em execuções efêmeras. Validado com a suíte inicial da Etapa 00. |
