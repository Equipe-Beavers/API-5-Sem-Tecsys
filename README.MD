![Banner Geomash](./assets/banner_geomash.png)
<br>

<p align="center">
  <b><a href="#sobre">📌 Sobre o projeto</a></b> &nbsp;&bull;&nbsp;
  <b><a href="#requisitos">📋 Requisitos</a></b> &nbsp;&bull;&nbsp;
  <b><a href="#backlog">🎯 Backlog</a></b> &nbsp;&bull;&nbsp;
  <b><a href="#tecnologias">🛠️ Tecnologias</a></b>
  <br>
  <b><a href="#entregas">🚀 Sprints</a></b> &nbsp;&bull;&nbsp;
  <b><a href="#dor-e-dod">✅ DoR & DoD</a></b> &nbsp;&bull;&nbsp;
  <b><a href="#links">🔗 Documentos</a></b> &nbsp;&bull;&nbsp;
  <b><a href="#equipe">👥 Equipe</a></b>
</p>
<span id="sobre">

# 📌 Sobre o projeto

Geomash é uma aplicação para planejamento e otimização da cobertura de radiofrequência em redes de distribuição de energia elétrica. A solução utiliza dados geográficos da BDGD para permitir a seleção dos ativos que necessitam de cobertura e, a partir de parâmetros técnicos e critérios de instalação, identificar e recomendar os locais mais adequados para instalação de gateways.

<span id="requisitos">

# 📋 Requisitos Funcionais

- **RF01 – Seleção da região de estudo:** O sistema deve permitir selecionar uma distribuidora e uma região geográfica, possibilitando a navegação por estado, município ou bairro e carregando somente os dados correspondentes à seleção.
- **RF02 – Visualização e consulta dos ativos da BDGD:** O sistema deve permitir visualizar os ativos da BDGD no mapa, aplicar filtros por tipo e consultar as informações disponíveis de cada ativo.
- **RF03 – Delimitação da área e seleção dos ativos de interesse:** O sistema deve permitir delimitar a área de interesse, considerando os ativos presentes nessa área e permitindo selecionar os ativos que necessitam de cobertura e definir suas prioridades.
- **RF04 – Criação e rastreabilidade do estudo:** O sistema deve permitir criar um estudo a partir da área selecionada, associando a distribuidora, região, ativos e registrando automaticamente a versão da BDGD utilizada.
- **RF05 – Configuração do Perfil de RF e gateway:** O sistema deve permitir selecionar ou configurar um Perfil de RF e gateway contendo características necessárias do equipamento.
- **RF06 – Configuração dos critérios de instalação:** O sistema deve permitir configurar critérios para determinar locais elegíveis à instalação de gateways.
- **RF07 – Análise e otimização dos locais candidatos:** O sistema deve identificar automaticamente os locais candidatos elegíveis e executar a otimização para selecionar uma combinação adequada de gateways.
- **RF08 – Visualização do resultado do estudo:** O sistema deve apresentar no mapa os gateways recomendados, suas manchas de cobertura e os ativos cobertos e não cobertos.
- **RF09 – Apresentação dos indicadores do estudo:** O sistema deve apresentar indicadores do resultado, incluindo quantidade de gateways, percentual de cobertura, ativos atendidos e não atendidos, capacidade utilizada por gateway e custo estimado.
- **RF10 – Avaliação e comparação de cenários:** O sistema deve permitir visualizar alternativas viáveis de implantação, ajustar parâmetros e recalcular o estudo, bem como comparar diferentes cenários por meio de seus principais resultados e indicadores.
- **RF11 – Armazenamento de cenários:** O sistema deve permitir salvar diferentes configurações e resultados como cenários de um mesmo estudo, preservando os parâmetros e a versão da BDGD utilizados em cada execução.
- **RF12 – Autenticação:** O sistema deve permitir a autenticação de usuários para acesso aos recursos persistentes da aplicação, como estudos salvos e Biblioteca.
- **RF13 – Persistência e gerenciamento de estudos:** O sistema deve permitir que usuários autenticados salvem e retomem seus estudos, restaurando suas configurações, estado de processamento e resultados, além de permitir renomear, duplicar e excluir estudos salvos.
- **RF14 – Biblioteca de itens reutilizáveis:** O sistema deve permitir cadastrar, consultar e reutilizar áreas de interesse, listas de ativos, Perfis de RF e gateway e critérios de instalação em diferentes estudos.


<span id="backlog">

# 🎯 Backlog do Produto

| **RF**   | **Rank** | **Prioridade** | **User Story**                                                                                                                                                                                                                                          | **Estimativa** | **Sprint** |
| -------- | -------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ---------- |
| **RF01** | 1        | Alta           | **Como planejador de cobertura,** quero consultar o mapa geoespacial consolidado com as informações da BDGD, para que eu tenha uma visão territorial precisa da rede e embase meus estudos de planejamento.                                             | 13             | Sprint 1   |
| **RF01** | 2        | Média          | **Como planejador de cobertura**, quero selecionar uma distribuidora e uma região, para acessar somente os dados geográficos relevantes ao meu estudo.                                                                                                  | 5              | Sprint 1   |
| **RF02** | 3        | Média          | **Como planejador de cobertura**, quero visualizar, filtrar e consultar os ativos da BDGD no mapa, para compreender a infraestrutura existente na região selecionada.                                                                                   | 5              | Sprint 1   |
| **RF03** | 4        | Alta           | **Como planejador de cobertura**, quero delimitar uma área de interesse, para restringir a análise à região que realmente desejo estudar.                                                                                                               | 13             | Sprint 1   |
| **RF04** | 5        | Alta           | **Como planejador de cobertura**, quero criar um estudo a partir da área e dos ativos selecionados, para organizar a análise e manter registrada a versão da BDGD utilizada.                                                                            | 8              | Sprint 1   |
| **RF08** | 6        | Alta           | **Como planejador de cobertura**, quero obter uma recomendação inicial dos locais para instalação de gateways, utilizando critérios e parâmetros predefinidos, para obter uma primeira sugestão de posicionamento para atender aos ativos selecionados. | 5              | Sprint 1   |
| **RF05** | 7        | Média          | **Como planejador de cobertura**, quero configurar o Perfil de RF e gateway do estudo, para que a cobertura e a capacidade sejam calculadas conforme o equipamento considerado.                                                                         | 5              | Sprint 2   |
| **RF06** | 8        | Média          | **Como planejador de cobertura**, quero configurar os critérios de instalação, para que somente locais tecnicamente permitidos sejam considerados como candidatos.                                                                                      | 5              | Sprint 2   |
| **RF08** | 9        | Alta           | **Como planejador de cobertura**, quero que o sistema estime a cobertura e a capacidade de atendimento de cada local candidato, para que a otimização considere quais ativos podem ser atendidos por cada gateway.                                      | 5              | Sprint 2   |
| **RF08** | 10       | Alta           | **Como planejador de cobertura**, quero executar e acompanhar a otimização considerando os parâmetros, critérios e restrições configurados no estudo, para obter uma combinação de gateways adequada ao cenário.                                        | 8              | Sprint 2   |
| **RF09** | 11       | Alta           | **Como planejador de cobertura**, quero visualizar no mapa os gateways recomendados, suas manchas de cobertura e os ativos atendidos e não atendidos, para compreender espacialmente o resultado da análise.                                            | 8              | Sprint 2   |
| **RF10** | 12       | Alta           | **Como planejador de cobertura**, quero visualizar os principais indicadores do estudo, incluindo percentual de cobertura, quantidade de gateways, capacidade utilizada e custo estimado, para avaliar quantitativamente a qualidade da solução.        | 5              | Sprint 2   |
| **RF11** | 13       | Média          | **Como planejador de cobertura**, quero ajustar os parâmetros do estudo e recalcular a solução, para avaliar o impacto das alterações sobre o resultado.                                                                                                | 5              | Sprint 2   |
| **RF11** | 14       | Média          | **Como planejador de cobertura**, quero visualizar alternativas de implantação, para avaliar outras combinações viáveis de gateways além da solução principal.                                                                                          | 5              | Sprint 2   |
| **RF13** | 15       | Média          | **Como usuário**, quero me autenticar na aplicação, para salvar estudos e utilizar os recursos persistentes.                                                                                                                                            | 5              | Sprint 3   |
| **RF14** | 16       | Baixa          | **Como planejador autenticado**, quero gerenciar meus estudos, para organizar e reutilizar análises anteriores.                                                                                                                                         | 5              | Sprint 3   |
| **RF15** | 17       | Média          | **Como planejador autenticado**, quero cadastrar e reutilizar itens na Biblioteca, para configurar novos estudos com mais rapidez e consistência.                                                                                                       | 5              | Sprint 3   |
| **RF12** | 18       | Alta           | **Como planejador de cobertura**, quero salvar diferentes configurações e resultados como cenários de um mesmo estudo, para preservar as alternativas analisadas.                                                                                       | 8              | Sprint 3   |
| **RF11** | 19       | Média          | **Como planejador de cobertura**, quero comparar diferentes cenários pelos seus principais resultados, para identificar qual configuração é mais adequada ao estudo.                                                                                    | 5              | Sprint 3   |

<span id="tecnologias">

# 🛠️ Tecnologias Utilizadas

![Dart](https://img.shields.io/badge/Dart-20232A?style=for-the-badge&logo=dart&logoColor=0175C2)
![Flutter](https://img.shields.io/badge/Flutter-20232A?style=for-the-badge&logo=flutter&logoColor=02569B)
![TypeScript](https://img.shields.io/badge/TypeScript-20232A?style=for-the-badge&logo=typescript&logoColor=3178C6)
![Python](https://img.shields.io/badge/Python-20232A?style=for-the-badge&logo=python&logoColor=3776AB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-20232A?style=for-the-badge&logo=postgresql&logoColor=4169E1)
![PostGIS](https://img.shields.io/badge/PostGIS-20232A?style=for-the-badge&logo=postgresql&logoColor=336791)
![Jira](https://img.shields.io/badge/Jira-20232A?style=for-the-badge&logo=jira&logoColor=0052CC)
![Google Workspace](https://img.shields.io/badge/Google%20Workspace-20232A?style=for-the-badge&logo=google&logoColor=4285F4)
![Figma](https://img.shields.io/badge/Figma-20232A?style=for-the-badge&logo=figma&logoColor=F24E1E)
![GitHub](https://img.shields.io/badge/GitHub-20232A?style=for-the-badge&logo=github&logoColor=FFFFFF)


<span id="entregas">

# 🚀 Entregas de Sprints

Cada entrega foi realizada a partir da criação de uma **tag** em cada repositório, além da criação de uma branch neste repositório com um relatório completo de tudo o que foi desenvolvido naquela sprint.
| Sprint | Previsão de entrega |      Status      | Histórico |
| :----: | :-----------------: | :--------------: | :-------: |
|   01   | 07/09/2026 a 27/09/2026 | ✅ Concluída  | [Ver relatório](https://github.com/Equipe-Beavers/API-5-Sem-Tecsys/tree/sprint1) |
|   02   |    05/10/2026 a 25/10/2026    |  ⭕ Não iniciada  |     —     |
|   03   |    02/11/2026 a 22/11/2026    |  ⭕ Não iniciada  |     —     |

<span id="dor-e-dod">

# ✅ DoR e DoD

## DoR (Definition of Ready) 

- **User Stories completas:** Todos os requisitos descritos em User Stories planejadas para caber na sprint.
- **Tarefas detalhadas e atribuídas:** Cada User Story deve ter ao menos uma task detalhada e atribuída a um responsável.
- **Critérios de aceitação definidos:** Cada User Story deve ter critérios de aceitação bem estabelecidos.
- **Estimativas definidas:** Todas as User Stories devem ter uma estimativa de esforço/tamanho feita pelo time
- **Wireframe/Mockup aprovados:** O cliente deve ter validado e aprovado os protótipos visuais.
- **Modelo de dados finalizado:** Estrutura de dados completamente definida e documentada.
- **Testes de aceitação definidos:** Incluindo testes sugeridos pelo cliente e testes de aceitação.
- **Ambiente de desenvolvimento pronto:** O time deve ter acesso a todos os ambientes, ferramentas e permissões necessárias.

<br>

## DoD (Definition of Done) 

- **Critérios de aceitação validados:** Todos os critérios de aceitação foram atendidos e verificados com testes apropriados.
- **Execução de testes adequados:** Testes unitários, de integração e de aceitação foram realizados para garantir a estabilidade e funcionamento correto da aplicação.
- **Código-fonte completo e padronizado:** O código está 100% implementado, refatorado e segue as boas práticas e padrões de qualidade definidos.
- **Commits organizados e documentados:** Os commits seguem a nomenclatura acordada, são claros, segmentados e possuem histórico bem documentado.
- **Guia de instalação detalhado:** A documentação de instalação é clara e completa, permitindo que qualquer usuário ou desenvolvedor configure e execute a aplicação sem dificuldades.
- **Manual do usuário disponível:** Um manual foi criado para orientar o cliente sobre o funcionamento da aplicação.


<span id="links">

# 🔗 Documentos úteis

- [Diagrama de Entidade-Relacionamento](./assets/Diagrama%20de%20Entidade-Relacionamento%20-%20Geomash.pdf)
- [Fluxo de trabalho no github](./assets/Fluxo%20de%20trabalho%20no%20Github%20-%20Equipe%20Beavers.pdf)
- [Termo de Compromisso e Regras de Permanência](./assets/Termo%20de%20Compromisso%20e%20Regras%20de%20Permanência%20na%20Equipe%20Beavers.pdf)

<span id="equipe">

# 👥 Equipe

| Nome | Contato | Papel |
| :--: | :---: | :---: |
| **Sarah Batagioti** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sarahbatagioti/) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/SarahBatagioti) | Product Owner |
| **Gustavo Almeida** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gualmeidac/) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/GustavoAC0802) | Scrum Master |
| **Guilherme Almeida** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/guilherme-almeida-profile/) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/AlmdGuilherme) | Dev Team |
| **Marianne Valério** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mariannevalerio/) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/mariannevalerion) | Dev Team |
| **Pedro Nicolau** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pedro-nicolau-b3883428a/) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/pedromnicolau) | Dev Team |
| **Francisco Rafael** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/francisco-rafael-pires/) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/franciscorafaelpires) | Dev Team |
| **Matheus de Castro** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/matheus-r-castro-70091a32b/) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/Matheus-Roberto-Castro) | Dev Team |