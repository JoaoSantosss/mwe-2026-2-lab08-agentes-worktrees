# Trilha de auditoria do agente da LogiTech

Cada linha é uma decisão tomada pelo Despachante do agente. Este arquivo é
escrito pelo código, não à mão: `agente/auditoria.py` acrescenta uma linha por
evento. `verificar.py` conta as linhas `AUTORIZADO` e `RECUSADO` daqui.

Vereditos possíveis:

- `AUTORIZADO`: os argumentos passaram no JSON Schema e o comando executou.
- `RECUSADO`: os argumentos não passaram no JSON Schema, ou a ferramenta não
  existe. **O comando não executou.**
- `FALHOU`: os argumentos passaram, o comando executou e o serviço respondeu
  com erro.

A tabela começa vazia. Ela se preenche sozinha à medida que você conversa com
o agente. Não edite as linhas à mão: uma trilha de auditoria editável pelo
auditado não é uma trilha de auditoria.

| Momento | Ferramenta | Veredito | Argumentos | Resultado |
|---|---|---|---|---|
| 2026-10-14T01:17:35 | consultar_status_pedido | AUTORIZADO | {} | {"atualizadoEm": "2026-10-14T00:54:08", "pedidoId": "PED-1042", "previsaoEntrega": "2026-10-16", "status": "EM_TRANSITO", "transportadora": "LogiTech Frota 0... |
| 2026-10-14T01:17:40 | consultar_status_pedido | AUTORIZADO | {} | {"atualizadoEm": "2026-10-14T00:54:08", "pedidoId": "PED-1042", "previsaoEntrega": "2026-10-16", "status": "EM_TRANSITO", "transportadora": "LogiTech Frota 0... |
