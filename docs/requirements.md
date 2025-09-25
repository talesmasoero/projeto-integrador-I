# Documento de Requisitos e Viabilidade

### 1. Introdução

Neste documento, detalhamos os requisitos levantados para o Dashboard Institucional e apresentamos a análise de viabilidade que realizamos. O objetivo deste trabalho foi definir um escopo claro e alcançável para o nosso Produto Mínimo Viável (MVP), focado inicialmente em atender às necessidades da coordenação pedagógica.

### 2. Pesquisa de Referência

Iniciamos o trabalho com uma pesquisa de referência em duas frentes: primeiro, analisamos dashboards de casos de uso específicos para entender a aplicação prática e, em segundo lugar, observamos as funcionalidades padrão nas principais ferramentas de mercado.

#### 2.1. Análise de Dashboards (Casos de Uso)

* **Exemplo A: Dashboard de Análise de Canal (YouTube Studio)**
    * **Insight para nosso projeto:** A importância de ter uma "visão geral" com os números mais importantes logo de cara e a necessidade de comparar dados em diferentes períodos de tempo.

* **Exemplo B: Dashboard de Vendas de E-commerce (Ex: Shopify Analytics)**
    * **Insight para nosso projeto:** O conceito de análise comparativa é o ponto-chave. Para nós, isso se traduz em cruzar dados para responder perguntas específicas. Por exemplo: poderemos comparar a frequência de um aluno com suas próprias menções para ver se há correlação com o desempenho. Além disso, poderemos analisar a frequência por disciplina para investigar por que os alunos de um curso faltam mais em determinada matéria. O "problema" é o conteúdo da disciplina ou talvez o professor que a leciona?

#### 2.2. Análise de Funcionalidades Padrão de Mercado

Para complementar, observamos as funcionalidades oferecidas por ferramentas líderes como **Power BI** e **Google Analytics**. Isso nos ajudou a entender o que é tecnicamente esperado de um dashboard moderno, como filtros complexos e alta interatividade (drill-down).

#### Conclusão da Pesquisa para o Projeto

Nossa pesquisa nos mostrou que um bom dashboard precisa:
1.  Apresentar os KPIs mais importantes de forma clara na tela inicial.
2.  Ter filtros por período como funcionalidade central.
3.  Permitir o cruzamento de dados para responder questões analíticas.
4.  Ser interativo, permitindo que o usuário explore os dados de forma intuitiva.

### 3. Levantamento de Requisitos (Checklist)

Com base na pesquisa e no foco na coordenação, definimos e priorizamos a seguinte lista de requisitos.

#### Requisitos Funcionais (RF)

| ID   | Descrição                                                                                      | Justificativa                                                                                      | Prioridade |
| :--- | :----------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------- | :--------- |
| RF01 | Exibir uma tela principal (overview) com KPIs: nº de alunos, frequência média e alunos em risco.   | Fornece uma visão gerencial rápida para a coordenação.                                             | **Alta** |
| RF02 | Permitir a aplicação de filtros por: período (data/mês/semestre), curso, disciplina e professor. | Essencial para análises específicas e aprofundadas.                                                | **Alta** |
| RF03 | Apresentar uma visualização detalhada por aluno, com seu histórico de presença e menções.        | Permite identificar padrões individuais para ações pedagógicas.                                    | **Alta** |
| RF04 | Permitir a visualização de dados por disciplina, mostrando a frequência média da turma.          | Ajuda a identificar se problemas de frequência são localizados.                                    | **Média** |
| RF05 | Permitir a exportação dos dados e gráficos da tela atual para um arquivo em formato PDF.         | Facilita o compartilhamento de relatórios com stakeholders externos.                               | **Baixa** |
| RF06 | Implementar um sistema de autenticação com diferentes níveis de acesso (coordenação, professor, aluno). | Essencial para a segurança em produção, mas pode ser implementado após o MVP inicial focado na coordenação. | **Baixa** |

#### Requisitos Não-Funcionais (RNF)

| ID    | Descrição                                                                      | Justificativa                                                                                          | Prioridade |
| :---- | :------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------- | :--------- |
| RNF01 | Garantir que o dashboard carregue os dados e gráficos em no máximo 5 segundos.    | Melhora a experiência do usuário e a usabilidade da ferramenta.                                        | **Alta** |
| RNF02 | Assegurar a conformidade do sistema com a LGPD.                                  | Requisito legal obrigatório para proteger a privacidade dos estudantes.                                | **Alta** |
| RNF03 | Desenvolver uma interface intuitiva, que não exija treinamento extensivo para ser utilizada. | Aumenta a probabilidade de adoção da ferramenta pela equipe.                                           | **Alta** |
| RNF04 | Garantir que o sistema seja responsivo para diferentes telas.                    | Foco inicial do MVP é a experiência em desktops. A responsividade completa será tratada como melhoria futura. | **Baixa** |

### 4. Matriz de Viabilidade (Focada no MVP)

Realizamos a análise de viabilidade sobre os requisitos de **prioridade alta**, que formam o nosso MVP (RF01, RF02, RF03).

| Requisito             | Viabilidade Técnica                                                                                               | Viabilidade Econômica                                                                                                | Viabilidade Operacional                                                                                                                                                                                                                                                        | Viabilidade Legal                                                                                                                                                                                                                                     | Decisão   |
| :-------------------- | :---------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------- |
| **RF01: Overview KPIs** | **Viável, com aprendizado.** A equipe possui conhecimento básico em frontend e análise de dados. Haverá uma curva de aprendizado com as tecnologias escolhidas, mas é um desafio alcançável. | **Viável.** O projeto utilizará linguagens de programação (Python, SQL) e ferramentas que possuem versões gratuitas para desenvolvimento (como o Power BI Desktop), resultando em custo zero de software. | **Viável.** A ferramenta otimiza o trabalho da coordenação não apenas por ser mais rápida, mas por consolidar informações de fontes diferentes (frequência, notas) em um só lugar, fornecendo uma visão mais completa e trabalhada do que a atual.     | **Viável.** A tela principal exibirá apenas dados agregados (médias, totais), sem expor informações individuais sensíveis, o que está em conformidade com as boas práticas de privacidade.                                                 | **INCLUIR** |
| **RF02: Filtros** | **Viável, com aprendizado.** A complexidade está na lógica do backend, mas é um problema comum e bem documentado em projetos de dados. | **Viável.** Sem custo de software adicional para implementar a lógica de filtragem.                                  | **Viável.** É a principal funcionalidade que dá poder ao usuário, permitindo que a coordenação explore os dados livremente para encontrar respostas.                                                                                                            | **Viável.** A questão legal aqui é sobre controle de acesso. Em versões futuras com múltiplos perfis, os filtros não poderiam permitir que um usuário (ex: professor) acesse dados de turmas que não são suas. Como o MVP é só para a coordenação (que tem acesso total), este risco é mitigado. | **INCLUIR** |
| **RF03: Detalhes do Aluno** | **Viável.** A consulta ao banco de dados para buscar um aluno específico é uma tarefa de baixa complexidade técnica. | **Viável.** Sem custo de software adicional.                                                                         | **Viável.** Esta tela aumenta drasticamente a eficiência operacional. Em vez de a coordenação ter que abrir uma planilha de notas e outra de frequência, ela terá uma visão unificada do aluno, o que agiliza o processo de análise e tomada de decisão. | **Requer Atenção.** Exibir dados individuais é um ponto sensível da LGPD. Para o MVP, o acesso será exclusivo da coordenação. Em versões futuras, será crucial ter um controle de acesso rigoroso para esta funcionalidade.                      | **INCLUIR** |

### 5. Considerações sobre Escopo e Limitações

A partir das análises, definimos o escopo do MVP, as funcionalidades para versões futuras e as limitações atuais do projeto.

* **Escopo do MVP:** O desenvolvimento irá focar na entrega de um dashboard para uso da coordenação, contendo a tela de overview com KPIs (RF01), os filtros para exploração de dados (RF02) e a visualização de detalhes por aluno (RF03).
* **Fora do Escopo (Versões Futuras):** Funcionalidades cruciais para a expansão do projeto, como o sistema de autenticação e diferentes níveis de acesso (RF06), ficaram para o futuro. Outras melhorias planejadas são a visualização por disciplina (RF04), exportação de relatórios (RF05) e responsividade para múltiplos dispositivos (RNF04).
* **Limitações do Projeto:** Detalhamos que o projeto se limita à camada de visualização e não inclui o sistema de coleta de dados. A qualidade do dashboard dependerá diretamente da qualidade dos dados que recebermos.

---

### 6. Reflexão

* **Quais requisitos são essenciais para o MVP?**
    Concluímos que os requisitos essenciais são RF01 (Overview), RF02 (Filtros) e RF03 (Detalhes do Aluno). Juntos, eles formam um ciclo de análise completo para a coordenação: ver o cenário geral, filtrar para investigar um ponto de atenção e, por fim, analisar o caso individual.

* **Quais podem ser incluídos em versões futuras?**
    A funcionalidade mais importante para o futuro é, sem dúvida, o sistema de login com diferentes permissões (RF06), que permitirá que professores e talvez até alunos acessem o sistema com segurança. Depois disso, vêm as demais melhorias de visualização (RF04) e utilidades (RF05).

* **Como a análise de viabilidade influenciou o escopo?**
    A análise foi fundamental para nos dar um "choque de realidade". A reavaliação da viabilidade técnica nos fez focar em um escopo menor e mais garantido. A decisão de  autenticação (RF06), após ponderar o foco exclusivo na coordenação, foi a maior mudança no escopo, permitindo concentrar todo o esforço da equipe nas funcionalidades de análise de dados, que são o coração do projeto.