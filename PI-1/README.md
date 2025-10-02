# PI-1 — Dashboard de Justificativa do Smart Attendance

## Visão geral
Este diretório reúne as 5 unidades de PI-1, com foco em coletar e analisar dados que justifiquem a adoção do Smart Attendance (chamada via QR dinâmico em janela sobreposta), entregando um dashboard com KPIs e visualizações alinhadas às dores mapeadas em sala.

## Objetivo de PI-1
Entregar um dashboard analítico que meça tempo de chamada tradicional, impacto de imprevistos e tempos de simulação de login (QR + credenciais fictícias), permitindo comparar cenários e estimar a economia de tempo e a redução de fricção na aula.

## Escopo e não-escopo
* **Escopo:** coleta observacional e simulada, dicionário de dados, protocolo de coleta, KPIs essenciais (frequência, tempo de chamada, dispersões) e visualizações com filtros por período, curso, disciplina e professor.
* **Fora do escopo:** implementação do sistema QR em produção, autenticação real multiperfil e integrações institucionais (endereçados nos próximos PIs).

## Estrutura das unidades
* `unidade-01/` — **Imersão, Ideação e Problema:** público-alvo, dores, oportunidades e métricas derivadas; inclui Mapa de Empatia, Jornadas e PM Canvas.
* `unidade-02/` — **Estratégia, Escopo e Tarefas:** requisitos priorizados do MVP do dashboard (RF01–RF03), dicionário de dados, protocolo e backlog.
* `unidade-03/` — **Integração entre Unidades:** conexão das ideias às histórias de usuário e aos dados; início da coleta piloto e gráficos exploratórios.
* `unidade-04/` — **Avaliação do problema real:** critérios para avaliar profundidade e relevância da análise no relatório de imersão, considerando complexidade do contexto organizacional/cliente.
* `unidade-05/` — **Integração entre disciplinas:** diretrizes para diálogo entre estatística, design, gestão e tecnologia garantindo coerência integrada ao longo das entregas.

## MVP do dashboard (PI-1)
* **RF01 — Overview:** KPIs de frequência média, tempo médio de chamada e turmas/alunos em risco, com comparação por período.
* **RF02 — Filtros:** período, curso, disciplina e professor; recortes por modalidade (lab/sala) e por tipo de imprevisto.
* **RF03 — Detalhe:** visão por turma/aluno em nível adequado ao MVP, com anonimização e foco analítico.

## Dados e qualidade
* **Dicionário de dados:** `aulas_observadas.csv` (tempo de chamada, imprevistos, presentes/total) e `simulacao_login.csv` (QR + login fictício, dispositivo/rede, erros/abandono).
* **Protocolo:** cronometragem padronizada, categorização de imprevistos, regras de privacidade (anonimização de RA/professor) e observações de campo.

## Riscos e mitigação
* **Qualidade/adesão de coleta:** piloto, checklist e dupla checagem; tratamento de outliers e lacunas.
* **Privacidade:** uso de dados agregados no MVP, anonimização e revisão ética simples conforme visão.

## Entregáveis
* **Documentos:** README das unidades, requisitos (MVP), dicionário de dados, protocolo de coleta e backlog.
* **Dados:** amostras CSV em `data/raw` e `data/processed` para alimentar o dashboard.
* **Visualizações:** KPIs e gráficos essenciais atendendo aos filtros e critérios de aceite.

## Próximos passos
Concluir coleta piloto, validar os gráficos e ajustar métricas conforme achados, então consolidar o dashboard final para apresentação de PI-1.