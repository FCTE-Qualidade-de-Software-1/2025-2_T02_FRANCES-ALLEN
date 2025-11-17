# Fase 3 - Projetar a Avaliação

## Plano de Avaliação

O objetivo desta fase é detalhar o Plano de Avaliação para as características de Confiabilidade e Portabilidade do site do Cebraspe, conforme definido na Fase 2. Este plano descreve o Método de Avaliação, os Recursos Necessários, o Cronograma de Ações e as Fontes de Evidência para a coleta sistemática dos dados das métricas (GQM) e a validação das hipóteses.

### 1. Método de Avaliação

Será utilizada uma abordagem mista, combinando:
- Análise quantitativa: coleta automatizada e semi-automatizada de métricas de desempenho e compatibilidade.
- Análise qualitativa: inspeção visual e manual para inconsistências de renderização e responsividade.

O método será estruturado em torno das métricas definidas na Fase 2, garantindo que cada métrica tenha um procedimento de coleta claro e rastreável.

### 1.1. Detalhamento do Método de Coleta por Métrica

A tabela abaixo detalha o plano de coleta para cada métrica definida na Fase 2.

### Confiabilidade

| Característica  | Métrica (GQM)                               | Ferramenta / Fonte de Dados                   | Plano de Coleta |
|-----------------|----------------------------------------------|-----------------------------------------------|------------------|
| Confiabilidade  | M1: Uptime do Site (%)                       | Serviço de Monitoramento (Ex: UptimeRobot, Pingdom)                        | 1. Configurar o monitoramento da URL principal (https://www.cebraspe.org.br/ ). <br> 2. Coletar o percentual de tempo de atividade (uptime) durante o período de avaliação (ex: 2 dias). <br> 3. Comparar o resultado com o critério de aceitação (H1.1: < 99,5% em picos de demanda). |
| Confiabilidade  | M2: Taxa de Erros HTTP 5xx sob Carga (%)     | Ferramenta de Teste de Carga (Ex: Apache JMeter, k6)                          | 1. Simular um cenário de alta demanda (ex: 80% da capacidade projetada ou um pico de acesso histórico). <br> 2. Executar o teste por um período definido (ex: 30 minutos). <br> 3. Coletar a proporção de respostas HTTP 5xx em relação ao total de requisições. <br> 4. Comparar com o critério de aceitação (H2.1: > 0,5%). |
| Confiabilidade  | M3: Tempo Médio para Recuperação (MTTR)      | Logs de Servidor / Histórico de Incidentes                | 1. Analisar o histórico de incidentes e falhas críticas (HTTP 5xx prolongados) no período de avaliação. <br> 2. Calcular o tempo médio entre a detecção da falha e a restauração completa do serviço. <br> 3. Comparar com o critério de aceitação (H3.1: > 30 minutos). Nota: Se não houver incidentes no período, a métrica será considerada atendida. |
| Confiabilidade  | M4: Taxa de Erros HTTP 5xx                   | Google Search Console / Logs de Acesso                  | 1. Coletar o número total de requisições e o número de erros HTTP 5xx em um período de baixa demanda (ex: 2 dias). <br> 2. Calcular o percentual de erros. <br> 3. Comparar com o critério de aceitação (H4.1: > 0,1% em 2 dias). |


### Portabilidade

| Característica | Métrica (GQM)                                   | Ferramenta / Fonte de Dados                        | Plano de Coleta |
|----------------|--------------------------------------------------|----------------------------------------------------|------------------|
| Portabilidade  | M1: Inconsistências de Renderização por Navegador |Inspeção Visual Manual / Ferramenta de Teste de Compatibilidade (Ex: BrowserStack, LambdaTest)         | 1. Selecionar os navegadores-alvo (Chrome, Firefox, Safari, Edge). <br> 2. Inspecionar visualmente as páginas principais (Home, Edital, Resultados) em cada navegador. <br> 3. Contar o número de inconsistências visuais ou funcionais (ex: elementos sobrepostos, quebra de CSS, scripts não executados). <br> 4. Comparar com o critério de aceitação (H1.1: Inconsistências em pelo menos 2 navegadores secundários). |
| Portabilidade  | M2: Percentual de Quebra de Layout em Mobile (%) | Ferramenta de Teste de Responsividade (DevTools do Chrome/Firefox)                      | 1. Utilizar o modo de inspeção de dispositivos móveis (DevTools) para simular diferentes tamanhos de tela (smartphone e tablet, modo retrato e paisagem). <br> 2. Inspecionar as páginas principais. <br> 3. Contar o número de telas ou componentes com falhas de layout (ex: texto cortado, rolagem horizontal).<br> 4. Calcular a proporção de telas com falhas. <br> 5. Comparar com o critério de aceitação (H2.1: Quebra de layout em telas de smartphone). |


### 2. Recursos Necessários

A execução da avaliação requer a mobilização de recursos humanos, materiais e ferramentas técnicas.

| Tipo de Recurso       | Recurso                                     | Descrição                                                                 |
|-----------------------|----------------------------------------------|---------------------------------------------------------------------------|
| Ferramentas Técnicas  | Serviço de Monitoramento de Uptime          | Plataforma para monitoramento contínuo da disponibilidade do site.        |
| Ferramentas Técnicas  | Ferramenta de Teste de Carga                | Software para simular múltiplos usuários simultâneos e medir o desempenho sob estresse. |
| Ferramentas Técnicas  | Ferramenta de Teste de Compatibilidade/Responsividade | Plataforma ou DevTools de navegadores para simular diferentes ambientes de execução (navegadores, dispositivos). |
| Ferramentas Técnicas  | Logs de Servidor / Google Search Console    | Fontes de dados para extrair métricas de erros HTTP 5xx e histórico de falhas. |
| Recursos Humanos      | Avaliadores Técnicos                        | Membros da equipe responsáveis pela configuração das ferramentas e execução dos testes de carga e compatibilidade. |
| Recursos Humanos      | Analistas de Qualidade                      | Membros da equipe responsáveis pela inspeção visual, coleta manual de dados e julgamento dos resultados. |
| Materiais de Apoio    | Documento GQM (Fase 2)                      | Roteiro formal com as métricas, hipóteses e critérios de aceitação.       |
| Materiais de Apoio    | Planilha de Coleta de Dados                 | Documento digital (Google Sheets/Excel) para registro dos dados brutos coletados. |


### 3. Cronograma de Ações

O cronograma proposto visa a coleta paralela dos dados de Confiabilidade e Portabilidade, seguida pela consolidação e análise.

| Etapa                                   | Responsável(eis)        | Prazo Estimado                               |
|----------------------------------------|--------------------------|----------------------------------------------|
| Configuração do Ambiente               | Avaliadores Técnicos     | Dia 1                                        |
| Coleta de Confiabilidade (M1, M4)      | Analistas de Qualidade   | Dias 1‒2 (Monitoramento Contínuo)            |
| Coleta de Confiabilidade (M2)          | Avaliadores Técnicos     | Dia 2 (Execução do Teste de Carga)          |
| Coleta de Confiabilidade (M3)          | Analistas de Qualidade   | Dias 1‒2 (Análise de Logs/Histórico)         |
| Coleta de Portabilidade (M1, M2)       | Avaliadores Técnicos     | Dias 3‒4 (Testes de Compatibilidade e Responsividade) |
| Consolidação dos Dados Brutos          | Analistas de Qualidade   | Dia 5                                        |
| Análise e Julgamento dos Resultados    | Todos                    | Dia 6                                        |
| Elaboração do Relatório da Fase 3      | Analistas de Qualidade   | Dia 7                                        |


### 4. Fontes de Evidência e Rastreabilidade

A rastreabilidade é crucial para garantir a validade e a auditabilidade da avaliação.

| Fonte de Evidência                     | Local/Ferramenta                                          | Uso                                                                 | Avaliação Esperada                                                  |
|----------------------------------------|------------------------------------------------------------|---------------------------------------------------------------------|--------------------------------------------------------------------|
| Definição da Avaliação (Fase 2)        | Documento GQM (Seção 1)                                    | Roteiro formal que define o que e como medir.                      | O plano de coleta deve ser 100% fiel ao GQM da Fase 2.             |
| Dados Brutos Coletados                 | Planilha de Coleta de Dados                                | Armazenamento dos resultados numéricos e qualitativos (ex: contagem de inconsistências, percentuais de uptime). | Garante a auditabilidade e a base para o julgamento.               |
| Relatórios de Ferramentas              | Logs de Teste de Carga, Relatórios de Uptime, Screenshots de Inconsistências | Evidências primárias da execução dos testes.                       | Valida a execução do método e fornece dados brutos.                |
| Relatório Final da Fase 3              | Documento desta Fase                                       | Consolidação do Plano de Avaliação e preparação para a Fase 4 (Execução). | Deve referenciar todas as fontes de evidência e o GQM.             |

### Histórico de Versões

| Versão | Descrição | Responsável | Data  | Revisor(es) | Detalhes da Revisão | Data da revisão |
| :----: | --------- | --------- | :--------------: | ----------- | :-------------: | :-------------: |
| `1.0` | documentação geral | [Maria Clara](https://github.com/alvezclari) | 17/11/2025|   |  |  |
