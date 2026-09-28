![Banner Geomash](./assets/banner_geomash.png)

<p align="center">
	<b><a href="#meta-da-sprint">📝 Meta da Sprint</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#objetivos-da-sprint">🎯 Objetivos</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#backlog-da-sprint">📃 Backlog</a></b> &nbsp;&bull;&nbsp;
	<b><a href="#metricas-do-time">📈 Métricas</a></b>
</p>

<span id="meta-da-sprint"></span>
# 📝 Meta da Sprint 

Permitir o fluxo completo de planejamento de gateways, desde a seleção da região e consulta de ativos da BDGD até a delimitação da área e a análise automática de locais candidatos - inicialmente usando dados padrões de configuração de perfil RF e critérios de instalação

<span id="objetivos-da-sprint"></span>
# 🎯 Objetivos da Sprint

Os requisitos funcionais atendidos nesta sprint foram:

- **✔️ RF01 – Seleção da região de estudo:** O sistema deve permitir selecionar uma distribuidora e uma região geográfica, possibilitando a navegação por estado, município ou bairro e carregando somente os dados correspondentes à seleção.
- **✔️ RF02 – Visualização e consulta dos ativos da BDGD:** O sistema deve permitir visualizar os ativos da BDGD no mapa, aplicar filtros por tipo e consultar as informações disponíveis de cada ativo.
- **✔️ RF03 – Delimitação da área e seleção dos ativos de interesse:** O sistema deve permitir delimitar a área de interesse, considerando os ativos presentes nessa área e permitindo selecionar os ativos que necessitam de cobertura.
- **✔️ RF04 – Criação e rastreabilidade do estudo:** O sistema deve permitir criar um estudo a partir da área selecionada, associando a distribuidora, região, ativos e registrando automaticamente a versão da BDGD utilizada.
- **✔️ RF05 – Configuração e Otimização de Gateways e Locais**: O sistema deve permitir a configuração de perfis de RF, gateways e critérios de instalação para identificar automaticamente locais candidatos elegíveis e otimizar a seleção da melhor combinação de gateways com base nesses parâmetros.

<span id="backlog-da-sprint"></span>
# 📃 Backlog da Sprint

<span id="rf01-rank-1"></span>
## 📌 RF01 — Rank 1 | Prioridade: Alta | Estimativa: 13 pts 
* **User Story:** **Como planejador de cobertura,** quero consultar o mapa geoespacial consolidado com as informações da BDGD, para que eu tenha uma visão territorial precisa da rede e embase meus estudos de planejamento.
* **Valor de Negócio / Impacto:** **Visão sistêmica:** Elimina o uso de múltiplas ferramentas desconectadas, garantindo que as decisões de engenharia sejam tomadas sobre uma base cartográfica única e confiável.

<span id="rf01-rank-1-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Localização Inicial Padrão (Com GPS Ativo):** Ao abrir a tela sem filtros definidos, o mapa deve carregar centralizado automaticamente na posição geográfica atual do usuário (caso a permissão de localização esteja concedida).
- **Estado Inicial da Camada de Dados:** Na abertura padrão, o mapa deve carregar sem nenhuma camadas visíveis para garantir o rápido carregamento inicial da tela.
- **Visualização do Mapa Geoespacial:** O sistema deve exibir a interface principal do mapa interativo com os elementos elétricos e territoriais da BDGD plotados geograficamente.
- **Busca Rápida de Ativos:** O sistema deve disponibilizar uma barra de pesquisa superior para buscar diretamente por nome ou código do alimentador ou município.
- **Atalhos e Filtros Rápidos:** O sistema deve apresentar seletores no topo da tela para alterar rapidamente a distribuidora ativa (ex: CEMIG D) e filtrar por Cidade / bairro, além de um botão dedicado para abrir o painel de camadas do mapa.
- **Controles de Navegação no Mapa:** O sistema deve disponibilizar botões flutuantes para aproximação (+), afastamento (-) e centralização da localização atual do usuário no mapa.
- **Início de Novo Estudo:** O sistema deve exibir um botão em destaque na parte inferior (+ Iniciar estudo) para permitir o avanço para o fluxo de planejamento e seleção de área.
- **Navegação Principal:** O sistema deve manter a barra de navegação inferior visível, permitindo o acesso direto às seções Início, Estudos, Biblioteca e Perfil.
- **Aplicação responsiva:** O sistema deve adaptar o layout e os elementos da interface automaticamente para garantir a usabilidade em dispositivos mobile, tablets e computadores.

<span id="rf01-rank-2"></span>
## 📌 RF01 — Rank 2 | Prioridade: Média | Estimativa: 5 pts 
* **User Story:** **Como planejador de cobertura**, quero selecionar uma distribuidora e uma região, para acessar somente os dados geográficos relevantes ao meu estudo.
* **Valor de Negócio / Impacto:** **Eficiência operacional:** Reduz o tempo de carregamento do sistema e foca a análise estritamente no escopo de interesse.

<span id="rf01-rank-2-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Seleção de Distribuidora (Passo 1):** O sistema deve listar as distribuidoras disponíveis para seleção, exibindo o nome, a UF, o ano da base BDGD vinculada e a quantidade total de ativos.
- **Busca de Distribuidora:** O sistema deve disponibilizar um campo de busca por texto para filtrar rapidamente a lista de distribuidoras por nome.
- **Seleção da Região/Município (Passo 2):** Após confirmar a distribuidora, o sistema deve permitir buscar e selecionar o município desejado (ex: Uberaba — MG), informando o número de bairros/regiões disponíveis.
- **Filtro por Bairros/Zonas:** O sistema deve exibir as opções de bairros pertencentes ao município selecionado, permitindo selecionar um ou mais locais para restringir a consulta.
- **Navegação e Ações do Fluxo:** O sistema deve exibir a indicação clara do progresso da etapa (PASSO 1 DE 4 e PASSO 2 DE 4), possibilitando voltar à etapa anterior, Limpar as seleções efetuadas ou acionar o botão Prosseguir para avançar no fluxo.
- **Campo de busca:** O sistema deve exibir um campo de busca para procurar uma cidade no mapa e direcionar o usuário.
- **Aplicação responsiva:** O sistema deve adaptar o layout e os elementos da interface automaticamente para garantir a usabilidade em dispositivos mobile, tablets e computadores.

<span id="rf02-rank-3"></span>
## 📌 RF02 — Rank 3 | Prioridade: Média | Estimativa: 5 pts 
* **User Story:** **Como planejador de cobertura**, quero visualizar, filtrar e consultar os ativos da BDGD no mapa, para compreender a infraestrutura existente na região selecionada.
* **Valor de Negócio / Impacto:** **Assertividade técnica:** Permite identificar rapidamente a infraestrutura existente.

<span id="rf02-rank-3-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Visualização de Ativos no Mapa:** O sistema deve renderizar graficamente no mapa a rede elétrica e seus respectivos ativos georreferenciados da BDGD, utilizando representações visuais e cores distintas para cada elemento.
- **Campo de busca por id:** O sistema deve disponibilizar um campo de busca onde, ao colocar o id do ativo, seja possível localizá-lo.
- **Painel de Controle de Camadas (Filtros):** O sistema deve disponibilizar um menu lateral de camadas agrupado por categorias de infraestrutura: Rede (ex: MT, BT, Neutro), Estruturas (ex: Poste, Transformador, Subestação), Proteção e Manobra (ex: Chave Fusível, Religador) e Regulação (ex: Regulador de Tensão, Banco de Capacitores).
- **Seleção e Aplicação de Camadas:** O sistema deve permitir ao usuário marcar ou desmarcar individualmente as camadas desejadas, exibir o contador de filtros ativos (ex: 7 de 12 camadas ativas), permitir a limpeza rápida das escolhas (Limpar) e atualizar o mapa ao acionar Salvar filtro.
- **Consulta e Detalhamento do Ativo:** Ao clicar em um elemento individual no mapa, o sistema deve abrir um card inferior (bottom sheet) apresentando os dados completos daquele ativo (ex: ID, status operacional, coordenadas Lat/Long, material, esforço/tração, ordem de imobilização, situação do ativo, subestação conectada e ponto de acesso).
- **Fechamento e Destaque Visual:** O sistema deve permitir fechar o painel de detalhes ou de filtros a qualquer momento através do botão de fechar (X), retornando a navegação livre e à visualização da área no mapa.
- **Fluxo:** O botão de camadas aparece somente depois dos filtros de região estarem definidos - ele pode ver os ativos da região de pesquisa, para não exibir geral.
- **Aplicação responsiva:** O sistema deve adaptar o layout e os elementos da interface automaticamente para garantir a usabilidade em dispositivos mobile, tablets e computadores.

<span id="rf03-rank-4"></span>
## 📌 RF03 — Rank 4 | Prioridade: Alta | Estimativa: 13 pts 
* **User Story:** **Como planejador de cobertura**, quero delimitar uma área de interesse, para restringir a análise à região que realmente desejo estudar.
* **Valor de Negócio / Impacto:** **Foco estratégico:** Otimiza o processamento de dados ao restringir o escopo geográfico da análise de cobertura.

<span id="rf03-rank-4-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Modos de Delimitação da Área:** O sistema deve oferecer diferentes métodos de seleção geográfica (Desenhar, Raio e Região), permitindo que o usuário escolha a forma ideal de delimitar a região.
- **Desenho Livre e Ajuste no Mapa:** Ao selecionar a opção de desenho, o sistema deve permitir ao usuário marcar e ajustar os vértices diretamente no mapa interativo para delimitar a área de interesse com precisão.
- **Visualização da Região e Contexto:** O sistema deve exibir o contexto do local selecionado no topo da tela (Distribuidora, Cidade, Bairro) e a indicação do progresso do fluxo (ex: PASSO 3 DE 4).
- **Métricas da Área em Tempo Real:** O sistema deve calcular e exibir instantaneamente o resumo da delimitação, incluindo o tamanho total da Área em km² (ex: 38,4 km²), a quantidade total de Ativos contidos nela (ex: 1.956) e o número de Alimentadores mapeados na região (ex: 6).
- **Opção de Redesenho:** O sistema deve disponibilizar a funcionalidade de Refazer dentro do painel da área selecionada para permitir ao usuário limpar a seleção atual e desenhar uma nova região do zero.
- **Ações de Navegação e Confirmação:** O sistema deve disponibilizar botões para Cancelar a operação ou Prosseguir, avançando no fluxo de criação do estudo com os dados geográficos e de ativos delimitados.
- **Aplicação responsiva:** O sistema deve adaptar o layout e os elementos da interface automaticamente para garantir a usabilidade em dispositivos mobile, tablets e computadores.

<span id="rf04-rank-5"></span>
## 📌 RF04 — Rank 5 | Prioridade: Alta | Estimativa: 8 pts 
* **User Story:** **Como planejador de cobertura**, quero criar um estudo a partir da área e dos ativos selecionados, para organizar a análise e manter registrada a versão da BDGD utilizada.
* **Valor de Negócio / Impacto:** **Organização e Padronização:** Consolida em um único fluxo os filtros de região e ativos com as configurações padrão, viabilizando a execução e a geração estruturada dos resultados do estudo.

<span id="rf04-rank-5-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Identificação do Estudo:** O sistema deve permitir ao usuário definir um nome para o estudo (ex: Zona Oeste — Religadores) para identificar e organizar a análise.
- **Definição de Perfil de RF e Gateway:** O sistema deve apresentar por padrão as configurações técnicas e financeiras de RF pré-definidas.
- **Parâmetros dos Critérios de Instalação:** O sistema deve exibir as regras padrão de instalação configuradas.
- **Seleção de Ativos a Cobrir:** O sistema deve permitir a seleção dos tipos de ativos que farão parte do estudo (ex: Religadores, Reguladores, Chaves fusível), atualizando o visual do ativo selecionado.
- **Contador em Tempo Real de Ativos:** O sistema deve exibir um resumo contendo a quantidade total de ativos presentes na área e o total exato de ativos selecionados para a análise (ex: 1.956 ativos na área / 612 selecionados).
- **Geração e Registro do Estudo:** Ao acionar o botão de ação principal (Criar estudo e simular), o sistema deve salvar as configurações, vincular a versão da BDGD ativa no momento do registro e iniciar o cálculo da simulação.
- **Aplicação responsiva:** O sistema deve adaptar o layout e os elementos da interface automaticamente para garantir a usabilidade em dispositivos mobile, tablets e computadores.

<span id="rf05-rank-6"></span>
## 📌 RF05 — Rank 6 | Prioridade: Alta | Estimativa: 5 pts 
* **User Story:** **Como planejador de cobertura**, quero obter uma recomendação inicial dos locais para instalação de gateways, utilizando critérios e parâmetros predefinidos, para obter uma primeira sugestão de posicionamento para atender aos ativos selecionados.
* **Valor de Negócio / Impacto:** **Agilidade e Escala:** Reduz drasticamente o esforço manual de engenharia de campo, permitindo uma simulação rápida, mesmo que com configurações padrões.

<span id="rf05-rank-6-criterios-de-aceitacao"></span>
### Critérios de Aceitação:
- **Geração de Recomendação Inicial:** O sistema deve calcular e apresentar uma proposta inicial de planejamento de cobertura ao selecionar a região, exibindo a área em km² e a localização genérica correspondente.
- **Resumo de Indicadores Principais (KPIs):** O sistema deve destacar no topo da tela o percentual total de Cobertura alcançado com a proposta, a quantidade necessária de Gateways e o Custo Total estimado para a implementação.
- **Status Geral de Ativos Atendidos:** O sistema deve apresentar uma barra visual de progresso informando a quantidade total de ativos elétricos cobertos em relação ao total de ativos da região (ex: 1.842 de 1.956).
- **Detalhamento de Ativos sem Cobertura por Categoria:** O sistema deve listar a quantidade de ativos atendidos e destacar claramente os que ficaram sem cobertura, categorizados por tipo (ex: Religadores, Reguladores de Tensão e Chaves Fusível).
- **Lista de Gateways Propostos:** O sistema deve exibir a lista rolável dos gateways sugeridos (ex: GW-14, GW-15), indicando a contagem atual e o total de gateways identificados.
- **Detalhamento do Ponto de Instalação do Gateway:** Cada cartão de gateway recomendado deve exibir a identificação do ativo de infraestrutura (ex: PST-80213, SE-00412), o endereço/local de instalação, as coordenadas geográficas (latitude/longitude), o tipo de ativo elétrico suporte (ex: Poste de MT, Subestação) e o alimentador ao qual pertence.
- **Aplicação responsiva:** O sistema deve adaptar o layout e os elementos da interface automaticamente para garantir a usabilidade em dispositivos mobile, tablets e computadores.

<span id="metricas-do-time"></span>
# 📈 Métricas do Time

A sprint, composta por 6 user stories e 22 tasks, registrou o progresso por meio de um gráfico de burndown que compara a taxa ideal com a real, onde o eixo X representa os dias trabalhados e o eixo Y indica as entregas e esforços. O pico de conclusão observado no final acontece porque as user stories só são contabilizadas no gráfico após 100% de sua finalização.

![Burndown](./assets/Burndown%20-%201°%20sprint.jpg)



