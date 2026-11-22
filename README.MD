![Banner Geomash](./assets/banner_geomash.png)

<p align="center">
	<b><a href="#meta-da-sprint">📌 Meta da Sprint</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#objetivos-da-sprint">🎯 Objetivos</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#backlog-da-sprint">📃 Backlog</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#metricas-do-time">📈 Métricas</a></b>
</p>

<span id="meta-da-sprint"></span>
# 📌 Meta da Sprint 

Habilitar a gestão individualizada de projetos através da autenticação de usuários, assegurando que cada perfil mantenha seu histórico de estudos, parâmetros de instalação e configurações de RF salvos para consultas e edições futuras.

<span id="objetivos-da-sprint"></span>
# 🎯 Objetivos da Sprint

Os requisitos funcionais atendidos nesta sprint foram:

- **✔️ RF10 - Autenticação e gerenciamento de estudos:** Foi implementado o fluxo de cadastro e login de usuários, com validação das credenciais e gerenciamento de sessão. Os estudos e suas configurações passaram a ser vinculados ao usuário autenticado, assegurando que cada pessoa acesse apenas seus próprios dados persistidos.
- **✔️ RF09 - Avaliação e comparação de cenários:** Foram disponibilizadas alternativas de implantação além da solução otimizada principal. O usuário pode selecionar cada cenário para consultar sua configuração, os gateways recomendados, a cobertura gerada e seus indicadores específicos.
- **✔️ RF07 - Análise e otimização dos locais candidatos:** A análise de elegibilidade e o cálculo de propagação passaram a considerar informações ambientais e geográficas, como relevo, vegetação, edificações, antenas e estruturas existentes. Esses fatores influenciam a seleção dos locais candidatos e a recomendação dos gateways.
- **✔️ RF08 - Exportação dos resultados do estudo:** Foi disponibilizada a exportação dos resultados de estudos processados em PDF. O arquivo reúne a identificação do estudo, a região analisada, os indicadores calculados e, quando aplicável, os resultados dos cenários alternativos.
- **✔️ RF02 - Importação de ativos para o estudo:** Foi implementada a importação de arquivos com ativos da região de interesse, em formatos compatíveis como CSV e GeoJSON. Os dados são validados, exibidos no mapa e associados ao estudo sem alterar a base BDGD original.

<span id="backlog-da-sprint"></span>
# 📃 Backlog da Sprint

<span id="rf10-rank-12"></span>
## 📌 RF10 - Rank 12 | Prioridade: Média | Estimativa: 5 pts

* **User Story:** **Como usuário,** quero me autenticar na aplicação, para salvar estudos e utilizar os recursos persistentes.

### Critérios de Aceitação:

- **Cadastro de usuário:** O sistema deve permitir o cadastro de novos usuários, solicitando as informações necessárias, como nome de usuário, e-mail e senha.
- **Validação de cadastro:** O sistema deve impedir o cadastro de e-mails ou nomes de usuário já existentes e validar o preenchimento dos campos obrigatórios.
- **Autenticação:** O sistema deve disponibilizar uma tela de login com e-mail e senha, permitindo o acesso aos recursos da aplicação após a validação das credenciais.
- **Validação de credenciais:** O sistema deve informar quando as credenciais forem inválidas, sem permitir o acesso aos recursos restritos.
- **Gerenciamento de sessão:** O sistema deve manter a sessão do usuário autenticado durante a navegação e disponibilizar uma opção para encerrar a sessão.
- **Isolamento de dados:** Cada usuário deve ter acesso somente aos seus próprios estudos salvos, impedindo a visualização ou alteração de estudos pertencentes a outros usuários.

<span id="rf09-rank-13"></span>
## 📌 RF09 - Rank 13 | Prioridade: Média | Estimativa: 5 pts

* **User Story:** **Como planejador de cobertura,** quero visualizar alternativas de implantação, para avaliar outras combinações viáveis de gateways além da solução principal.

### Critérios de Aceitação:

- **Geração de alternativas:** O sistema deve disponibilizar 5 alternativas de implantação, além da configuração otimizada principal.
- **Identificação dos cenários:** O sistema deve identificar claramente a configuração otimizada e as alternativas disponíveis, permitindo diferenciá-las.
- **Seleção de cenário:** O sistema deve permitir selecionar uma alternativa para visualizar seus resultados individualmente.
- **Visualização geográfica:** Ao selecionar um cenário, o mapa deve atualizar a localização dos gateways recomendados, suas respectivas manchas de cobertura e os ativos atendidos e não atendidos.
- **Indicadores por cenário:** O sistema deve apresentar os principais indicadores de cada alternativa, incluindo quantidade de gateways, percentual de cobertura, quantidade de ativos atendidos e não atendidos e capacidade utilizada.
- **Consistência dos resultados:** Cada cenário deve apresentar seus próprios resultados, garantindo que a seleção de uma alternativa não altere indevidamente os dados de outro cenário.

<span id="rf07-rank-14"></span>
## 📌 RF07 - Rank 14 | Prioridade: Alta | Estimativa: 8 pts

* **User Story:** **Como planejador de cobertura,** quero que as informações de relevo, antenas e estruturas existentes, vegetação e edifícios sejam consideradas na análise dos locais candidatos e no cálculo de propagação de RF, para que a otimização recomende gateways considerando as características reais do ambiente.

### Critérios de Aceitação:

- **Dados de relevo:** O sistema deve utilizar informações de elevação do terreno para identificar variações topográficas que possam influenciar a propagação do sinal de RF.
- **Dados de vegetação:** O sistema deve considerar a presença de vegetação na região de estudo como possível fonte de atenuação do sinal.
- **Dados de edificações:** O sistema deve identificar construções e estruturas que possam representar obstáculos à propagação do sinal ou inviabilizar determinados locais de instalação.
- **Dados de antenas e infraestrutura existente:** O sistema deve considerar informações disponíveis sobre antenas e estruturas existentes na região, avaliando sua influência na escolha dos locais candidatos e no planejamento da cobertura.
- **Influência na propagação de RF:** Os dados geográficos e ambientais disponíveis devem ser utilizados no cálculo de propagação, aplicando as respectivas condições de atenuação ou bloqueio quando pertinentes.
- **Influência na seleção de candidatos:** A análise das características ambientais deve influenciar a identificação e a elegibilidade dos locais candidatos à instalação dos gateways.
- **Integração com a otimização:** O algoritmo de otimização deve utilizar os resultados da análise ambiental para selecionar os gateways, em vez de considerar exclusivamente a distância entre os pontos.
- **Disponibilidade dos dados:** Caso alguma fonte de informação geográfica ou ambiental não esteja disponível para determinada região, o sistema deve permitir a continuidade do estudo, sem apresentar dados inexistentes como informações confirmadas.

<span id="rf08-rank-15"></span>
## 📌 RF08 - Rank 15 | Prioridade: Baixa | Estimativa: 5 pts

* **User Story:** **Como planejador de cobertura,** quero exportar os resultados do estudo em um arquivo PDF, para compartilhar as informações e os resultados do planejamento fora da aplicação.

### Critérios de Aceitação:

- **Opção de exportação:** O sistema deve disponibilizar uma opção para realizar o download em PDF dos resultados de um estudo processado.
- **Identificação do estudo:** O arquivo exportado deve apresentar informações de identificação do estudo, incluindo seu nome, região analisada e data de geração.
- **Indicadores do estudo:** A exportação deve incluir os principais indicadores calculados, como quantidade de gateways utilizados, percentual de cobertura, quantidade de ativos atendidos e não atendidos e capacidade utilizada.
- **Resultados de cenários alternativos:** Quando disponíveis, o sistema deve permitir incluir os resultados das alternativas de implantação na exportação.
- **Disponibilidade do download:** Após a geração do arquivo, o sistema deve disponibilizar o download diretamente pela interface da aplicação.
- **Integridade dos dados:** As informações exportadas devem corresponder aos resultados efetivamente calculados e apresentados no estudo, sem divergências entre os dados do arquivo e os dados da aplicação.

<span id="rf02-rank-16"></span>
## 📌 RF02 - Rank 16 | Prioridade: Baixa | Estimativa: 5 pts

* **User Story:** **Como planejador de cobertura,** quero importar um arquivo contendo os ativos que serão utilizados no estudo, para personalizar a análise com dados de uma versão específica da BDGD ou de uma região de interesse, em vez de utilizar exclusivamente os dados disponibilizados automaticamente pela aplicação.

### Critérios de Aceitação:

- **Importação de arquivo:** O sistema deve disponibilizar uma opção para selecionar e enviar um arquivo contendo os ativos que serão utilizados no estudo.
- **Formatos suportados:** O sistema deve aceitar arquivos em formatos geográficos compatíveis com a aplicação, como CSV e GeoJSON, respeitando a estrutura de dados esperada.
- **Validação do arquivo:** O sistema deve verificar se o arquivo possui os campos obrigatórios, informações geográficas válidas e estrutura compatível com o processamento.
- **Identificação dos ativos:** O sistema deve interpretar os registros importados, identificando suas coordenadas, tipos e demais atributos necessários para a análise.
- **Visualização dos ativos importados:** Após a importação, o sistema deve apresentar os ativos no mapa, permitindo verificar sua distribuição geográfica e as informações disponíveis.
- **Integração com o estudo:** Os ativos importados devem ser associados ao estudo correspondente e utilizados nas etapas de seleção, análise de cobertura e otimização dos gateways.
- **Preservação dos dados originais:** A importação não deve modificar ou sobrescrever a base BDGD original disponibilizada pela aplicação.

<span id="metricas-do-time"></span>
# 📈 Métricas do Time

A sprint, composta por 5 user stories e 14 tasks, registrou o progresso por meio de um gráfico de burndown que compara a taxa ideal com a real, onde o eixo X representa os dias trabalhados e o eixo Y indica as entregas e esforços. O pico de conclusão observado no final acontece porque as tasks só são contabilizadas no gráfico após 100% de sua finalização - com revisão de código, ajustes necessário e ai sim integração.

![Burndown](./assets/Burndown%20-%203°%20sprint.png)

