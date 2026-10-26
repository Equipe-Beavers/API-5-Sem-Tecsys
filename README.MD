![Banner Geomash](./assets/banner_geomash.png)

<p align="center">
	<b><a href="#meta-da-sprint">📝 Meta da Sprint</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#objetivos-da-sprint">🎯 Objetivos</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#backlog-da-sprint">📃 Backlog</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#metricas-do-time">📈 Métricas</a></b>
</p>

<span id="meta-da-sprint"></span>
# 📝 Meta da Sprint 

Permitir que o usuário personalize os estudos por meio da seleção de perfis de RF e critérios de instalação próprios, substituindo as configurações padrão por parâmetros adequados às características dos equipamentos e às condições de instalação. Dessa forma, o sistema poderá gerar recomendações de posicionamento de gateways mais alinhadas às necessidades de cada estudo.

<span id="objetivos-da-sprint"></span>
# 🎯 Objetivos da Sprint

Os requisitos funcionais atendidos nesta sprint foram:

- **✔️ RF05 – Configuração do Perfil de RF e gateway e reutilização de itens da Biblioteca:** O sistema deve permitir selecionar ou configurar um Perfil de RF e gateway contendo as características necessárias do equipamento, bem como cadastrar, consultar e reutilizar Perfis de RF e gateway, critérios de instalação, áreas de interesse e listas de ativos disponibilizados na Biblioteca em diferentes estudos.
- **✔️ RF06 – Configuração dos critérios de instalação:** O sistema deve permitir configurar critérios para determinar locais elegíveis à instalação de gateways, possibilitando o uso de critérios previamente cadastrados na Biblioteca.
- **✔️ RF07 – Análise e otimização dos locais candidatos:** O sistema deve identificar automaticamente os locais candidatos elegíveis e executar a otimização para selecionar uma combinação adequada de gateways. Devem ser considerados o relevo, os edifícios, as antenas e a vegetação do local do estudo.
- **✔️ RF08 – Visualização dos resultados e indicadores do estudo:** O sistema deve apresentar no mapa os gateways recomendados, suas manchas de cobertura e os ativos cobertos e não cobertos, além de indicadores como quantidade de gateways, percentual de cobertura, ativos atendidos e não atendidos, capacidade utilizada por gateway e custo estimado.

<span id="backlog-da-sprint"></span>
# 📃 Backlog da Sprint

<span id="rf05-rank-7"></span>
## 📌 RF05 — Rank 7 | Prioridade: Média | Estimativa: 5 pts
* **User Story:** **Como planejador de cobertura,** quero configurar o Perfil de RF e gateway do estudo, para que a cobertura e a capacidade sejam calculadas conforme o equipamento considerado.

<span id="rf05-rank-7-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Cadastro do Perfil de RF:** O sistema deve permitir criar um Perfil de RF com os parâmetros necessários para caracterizar o gateway utilizado na análise.
- **Parâmetros do Gateway:** O sistema deve permitir informar o nome da configuração, frequência de operação (MHz), potência de transmissão (dBm), sensibilidade de recepção (dBm), altura do gateway/ERB em relação ao solo (m), altura do dispositivo/ativo em relação ao solo (m), ganho ou atenuação adicional (dB, opcional) e quantidade máxima de ativos atendidos por gateway (opcional).
- **Fatores de propagação:** O sistema deve permitir considerar relevo, vegetação e demais fatores de atenuação ou bloqueio do sinal, conforme os dados disponíveis e o modelo de propagação utilizado.
- **Validação dos parâmetros:** O sistema deve validar os valores informados e impedir o processamento quando houver parâmetros obrigatórios ausentes ou inválidos.
- **Edição e exclusão do Perfil:** O usuário deve poder alterar os parâmetros do Perfil de RF e excluir o cadastro quando necessário.
- **Associação ao estudo:** O Perfil de RF selecionado/configurado deve ficar vinculado ao estudo e ser utilizado no processamento da cobertura e da otimização.
- **Integração com o cálculo de propagação:** O cálculo de perda de propagação deve utilizar os parâmetros definidos no Perfil de RF, substituindo valores fixos ou padrão quando configurados pelo usuário.
- **Persistência:** Ao salvar o estudo, o sistema deve manter uma cópia dos parâmetros do Perfil de RF utilizados na análise, permitindo identificar posteriormente a configuração considerada, mesmo após a edição ou exclusão do perfil original.
- **Aplicação responsiva:** O sistema deve adaptar o layout dos elementos de configuração para garantir a usabilidade em computadores, tablets e dispositivos mobile.

<span id="rf06-rank-8"></span>
## 📌 RF06 — Rank 8 | Prioridade: Média | Estimativa: 8 pts
* **User Story:** **Como planejador de cobertura,** quero configurar os critérios de instalação, para que somente locais tecnicamente permitidos sejam considerados como candidatos.

<span id="rf06-rank-8-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Configuração dos critérios:** O sistema deve permitir configurar os critérios que determinam se um local pode ser considerado elegível para instalação de um gateway.
- **Tipos de locais permitidos e proibidos:** O sistema deve permitir definir os tipos de locais ou estruturas permitidos e os locais ou condições que impedem a instalação.
- **Critério de alimentação:** O sistema deve permitir configurar se o local candidato necessita possuir disponibilidade de alimentação elétrica.
- **Critério de distância:** O sistema deve permitir configurar uma distância máxima aplicável à seleção dos locais candidatos.
- **Critérios ambientais:** O sistema deve permitir utilizar informações de relevo, vegetação e edificações na avaliação de elegibilidade, conforme as regras definidas para o estudo.
- **Critério de antenas e infraestrutura:** O sistema deve permitir considerar informações de antenas ou estruturas existentes quando forem relevantes para a análise.
- **Pesquisa das fontes de dados:** Antes da implementação de cada fonte externa, deve ser realizada análise técnica sobre disponibilidade, cobertura, formato, limitações de acesso e viabilidade de uso dos dados de relevo, vegetação, edificações e antenas.
- **Integração dos dados geográficos:** Os dados externos selecionados devem ser processados e disponibilizados ao mecanismo de avaliação dos candidatos dentro da área do estudo.
- **Avaliação de elegibilidade:** O sistema deve avaliar os possíveis locais de instalação de acordo com os critérios configurados e classificá-los como elegíveis ou não elegíveis.
- **Geração dos candidatos:** Somente os locais que atenderem aos critérios configurados devem compor o conjunto de candidatos disponibilizado para a otimização.
- **Identificação das restrições:** Quando um local não for elegível, o sistema deve identificar o critério que ocasionou sua restrição, permitindo rastrear a decisão.
- **Persistência dos critérios:** Os critérios utilizados devem ser armazenados juntamente com o estudo para garantir a rastreabilidade da configuração usada no processamento.

<span id="rf07-rank-9"></span>
## 📌 RF07 — Rank 9 | Prioridade: Média | Estimativa: 13 pts
* **User Story:** **Como planejador de cobertura,** quero executar e acompanhar a otimização considerando os parâmetros, critérios e restrições configurados no estudo, para obter uma combinação de gateways adequada ao cenário.

<span id="rf07-rank-9-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Execução do estudo:** O sistema deve permitir iniciar o processamento da otimização após a configuração do Perfil de RF e dos critérios de instalação.
- **Validação antes do processamento:** O sistema deve verificar se todos os parâmetros obrigatórios para a execução foram configurados antes de iniciar a otimização.
- **Candidatos elegíveis:** O algoritmo deve utilizar somente os locais classificados como elegíveis pelos critérios de instalação.
- **Integração com o algoritmo da Sprint 1:** O algoritmo existente de perda de propagação e seleção de gateways deve ser utilizado como base para a nova otimização, sem considerar locais eliminados pelos critérios de instalação.
- **Consideração do Perfil de RF:** A análise deve utilizar os parâmetros do Perfil de RF configurado para o estudo.
- **Consideração da cobertura e capacidade:** A otimização deve considerar a capacidade de cada candidato de atender aos ativos selecionados dentro das condições de propagação estabelecidas.
- **Consideração das prioridades:** Quando houver prioridades definidas para os ativos, o algoritmo deve considerá-las na seleção da solução.
- **Respeito às restrições:** A combinação final de gateways não deve conter locais que violem os critérios de instalação configurados.
- **Seleção da combinação:** O sistema deve selecionar uma combinação de gateways entre os candidatos elegíveis, buscando atender aos objetivos definidos para o estudo.
- **Acompanhamento do processamento:** O sistema deve informar o estado do processamento e disponibilizar o resultado quando a otimização for concluída.
- **Tratamento de ausência de solução:** Caso não existam candidatos elegíveis ou não seja possível obter uma solução dentro das restrições configuradas, o sistema deve informar claramente essa situação ao usuário.

<span id="rf08-rank-10"></span>
## 📌 RF08 — Rank 10 | Prioridade: Alta | Estimativa: 5 pts
* **User Story:** **Como planejador de cobertura,** quero visualizar no mapa os gateways recomendados, suas manchas de cobertura e os ativos atendidos e não atendidos, para compreender espacialmente o resultado da análise.

<span id="rf08-rank-10-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Exibição dos gateways:** Após a conclusão da otimização, o sistema deve apresentar no mapa a localização dos gateways recomendados.
- **Mancha de cobertura:** O sistema deve representar no mapa a área de cobertura associada a cada gateway recomendado.
- **Relação gateway × cobertura:** O usuário deve conseguir identificar qual área de cobertura pertence a cada gateway recomendado.
- **Ativos cobertos e não cobertos:** O sistema deve destacar os ativos atendidos e diferenciar os ativos que permaneceram sem cobertura.
- **Visualização conjunta:** O mapa deve permitir visualizar simultaneamente gateways, manchas de cobertura e ativos analisados.
- **Consulta do gateway:** O usuário deve poder selecionar um gateway no mapa e visualizar informações relacionadas à sua solução de cobertura.
- **Aplicação responsiva:** A visualização dos gateways, manchas e ativos deve permanecer utilizável em computadores, tablets e dispositivos mobile.

<span id="rf09-rank-11"></span>
## 📌 RF09 — Rank 11 | Prioridade: Média | Estimativa: 13 pts
* **User Story:** **Como planejador de cobertura,** quero visualizar informações geográficas e ambientais da região de estudo no mapa, para identificar características do terreno, estruturas existentes e possíveis obstáculos que influenciem o planejamento da cobertura de RF.

<span id="rf09-rank-11-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Camadas geográficas e ambientais:** O sistema deve permitir visualizar as camadas de relevo, vegetação, edificações e antenas, que são fatores relevantes à propagação do sinal.
- **Controle de camadas:** O usuário deve poder ativar, desativar e combinar as camadas, com identificação visual clara de cada tipo de informação.
- **Legenda e simbologia:** O mapa deve apresentar legenda, escala e simbologia consistente para que o usuário interprete corretamente as informações exibidas.
- **Consulta de elementos:** O usuário deve poder selecionar um elemento geográfico ou ambiental e visualizar seus atributos relevantes, como tipo, localização, altura, classificação ou fonte dos dados, quando disponíveis.
- **Aplicação responsiva:** O layout, os controles de camadas, a legenda e as consultas devem permanecer utilizáveis em computadores, tablets e dispositivos mobile.


<span id="metricas-do-time"></span>
# 📈 Métricas do Time

A sprint, composta por 5 user stories e 25 tasks, registrou o progresso por meio de um gráfico de burndown que compara a taxa ideal com a real, onde o eixo X representa os dias trabalhados e o eixo Y indica as entregas e esforços. O pico de conclusão observado no final acontece porque as tasks só são contabilizadas no gráfico após 100% de sua finalização - com revisão de código, ajustes necessário e ai sim integração.

![Burndown](./assets/Burndown%20-%202°%20sprint.jpg)

