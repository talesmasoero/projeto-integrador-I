# Unidade 2 — Estratégia, Escopo e Tarefas (MVP do Dashboard)

## Objetivo do MVP (PI-1)
Entregar um dashboard analítico que justifique a adoção do Smart Attendance, medindo tempo de chamada, impacto de imprevistos e tempos de simulação de login, com filtros essenciais e visão detalhada mínima, priorizando privacidade e viabilidade.

## Requisitos priorizados (MVP)
* **RF01 — Overview:** exibir KPIs de frequência média, tempo médio de chamada e turmas/alunos em risco, com comparação por período.
    * **Critério de aceite:** KPIs atualizam ao alterar filtros de período.
* **RF02 — Filtros:** período, curso, disciplina e professor, com visualizações por modalidade e tipo de imprevisto.
    * **Critério de aceite:** gráficos respondem a todos os filtros combinados.
* **RF03 — Detalhe:** visão por turma/aluno em nível adequado ao MVP, mantendo anonimização e foco analítico.
    * **Critério de aceite:** abrir detalhe exibe histórico agregado e respeita privacidade.

## Escopo IN/OUT
* **IN:** ingestão de CSV observacionais e simulados; transformações mínimas; KPIs e gráficos essenciais; anonimização; documentação do dicionário de dados e protocolo.
* **OUT:** autenticação real, integrações com sistemas institucionais, QR rotativo em produção, relatórios avançados e exportações complexas (ficam para próximos PIs).

## Dados e qualidade
* **Dicionário de dados:** `aulas_observadas.csv` e `simulacao_login.csv` com tipos, unidades, regras de preenchimento e validações.
* **Protocolo de coleta:** cronometragem por aula, categorização de imprevistos, registro de presentes/total, simulações com RA/senha fictícios, tratamento de fuso e observações.

## Backlog inicial
* **Coordenação:** ver tempo médio de chamada por turma e economia potencial por período para priorizar adoção.
    * **Aceite:** KPI e gráfico comparativo funcionando com filtros.
* **Professora:** avaliar impacto de imprevistos no tempo por disciplina e horário.
    * **Aceite:** gráfico de barras por tipo de imprevisto com variação clara.
* **Analista:** inspecionar distribuição de tempo de login simulado para dimensionar janela do QR.
    * **Aceite:** histograma/percentis por dispositivo/rede.

## Riscos e mitigações
* **Qualidade/adesão da coleta:** padronizar protocolo, fazer piloto e revisar outliers.
    * **Mitigação:** checklist e dupla checagem.
* **Privacidade:** anonimizar RA/professor e manter dados agregados no MVP.
    * **Mitigação:** seção LGPD e revisão ética simples.

## Entregáveis desta unidade
* `requisitos.md` revisado para MVP RF01–RF03.
* `escopo-mvp.md` com critérios de aceite por RF.
* `dicionario-de-dados.md` para os dois CSVs.
* `protocolo-de-coleta.md` com passo a passo e anonimização.
* `backlog.md` com histórias ligadas às métricas e gráficos.

## Direcionamento para a unidade 3
A partir dos requisitos e dados definidos, conectar as dores e hipóteses às histórias priorizadas, iniciar coleta piloto e gerar primeiros gráficos exploratórios para validar o desenho do dashboard.