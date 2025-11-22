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
| Confiabilidade  | M1: Uptime do Site (%)                       | Serviço de Monitoramento (UptimeRobot)                        | 1. Configurar o monitoramento da URL principal (https://www.cebraspe.org.br/ ). <br> 2. Coletar o percentual de tempo de atividade (uptime) durante o período de avaliação (ex: 2 dias). <br> 3. Comparar o resultado com o critério de aceitação (H1.1: < 99,5% em picos de demanda). |
| Confiabilidade  | M2: Taxa de Erros HTTP 5xx sob Carga (%)     | Ferramenta de Teste de Carga (Apache JMeter)                          | 1. Simular um cenário de alta demanda (ex: 80% da capacidade projetada ou um pico de acesso histórico). <br> 2. Executar o teste por um período definido (ex: 30 minutos). <br> 3. Coletar a proporção de respostas HTTP 5xx em relação ao total de requisições. <br> 4. Comparar com o critério de aceitação (H2.1: > 0,5%). |
| Confiabilidade  | M3: Tempo Médio para Recuperação (MTTR)      | Simulação de Logs de Servidor / Histórico de Incidentes                | 1. Analisar o histórico de incidentes e falhas críticas (HTTP 5xx prolongados) no período de avaliação. <br> 2. Calcular o tempo médio entre a detecção da falha e a restauração completa do serviço. <br> 3. Comparar com o critério de aceitação (H3.1: > 30 minutos). Nota: Se não houver incidentes no período, a métrica será considerada atendida. |
| Confiabilidade  | M4: Taxa de Erros HTTP 5xx                   | Simulação do Google Search Console / Logs de Acesso                  | 1. Coletar o número total de requisições e o número de erros HTTP 5xx em um período de baixa demanda (ex: 2 dias). <br> 2. Calcular o percentual de erros. <br> 3. Comparar com o critério de aceitação (H4.1: > 0,1% em 2 dias). |


### Portabilidade

| Característica | Métrica (GQM)                                   | Ferramenta / Fonte de Dados                        | Plano de Coleta |
|----------------|--------------------------------------------------|----------------------------------------------------|------------------|
| Portabilidade  | M1: Inconsistências de Renderização por Navegador |Inspeção Visual Manual / Ferramenta de Teste de Compatibilidade (BrowserStack)         | 1. Selecionar os navegadores-alvo (Chrome, Firefox, Safari, Edge). <br> 2. Inspecionar visualmente as páginas principais (Home, Edital, Resultados) em cada navegador. <br> 3. Contar o número de inconsistências visuais ou funcionais (ex: elementos sobrepostos, quebra de CSS, scripts não executados). <br> 4. Comparar com o critério de aceitação (H1.1: Inconsistências em pelo menos 2 navegadores secundários). |
| Portabilidade  | M2: Percentual de Quebra de Layout em Mobile (%) | Ferramenta de Teste de Responsividade (DevTools)                      | 1. Utilizar o modo de inspeção de dispositivos móveis (DevTools) para simular diferentes tamanhos de tela (smartphone e tablet, modo retrato e paisagem). <br> 2. Inspecionar as páginas principais. <br> 3. Contar o número de telas ou componentes com falhas de layout (ex: texto cortado, rolagem horizontal).<br> 4. Calcular a proporção de telas com falhas. <br> 5. Comparar com o critério de aceitação (H2.1: Quebra de layout em telas de smartphone). |


### 2. Recursos Necessários

A execução da avaliação requer a mobilização de recursos humanos, materiais e ferramentas técnicas.

| Tipo de Recurso       | Recurso                                     | Descrição                                                                 |
|-----------------------|----------------------------------------------|---------------------------------------------------------------------------|
| Ferramentas Técnicas  | Serviço de Monitoramento de Uptime          | Plataforma para monitoramento contínuo da disponibilidade do site.        |
| Ferramentas Técnicas  | Ferramenta de Teste de Carga                | Software para simular múltiplos usuários simultâneos e medir o desempenho sob estresse. |
| Ferramentas Técnicas  | Ferramenta de Teste de Compatibilidade/Responsividade | Plataforma ou DevTools de navegadores para simular diferentes ambientes de execução (navegadores, dispositivos). |
| Recursos Humanos      | Avaliadores Técnicos                        | Membros da equipe responsáveis pela configuração das ferramentas e execução dos testes de carga e compatibilidade. |
| Recursos Humanos      | Analistas de Qualidade                      | Membros da equipe responsáveis pela inspeção visual, coleta manual de dados e julgamento dos resultados. |
| Materiais de Apoio    | Documento GQM (Fase 2)                      | Roteiro formal com as métricas, hipóteses e critérios de aceitação.       |


### 3. Cronograma de Ações

O cronograma proposto visa a coleta paralela dos dados de Confiabilidade e Portabilidade, seguida pela consolidação e análise.

| Etapa                                   | Responsável(eis)        | Prazo Estimado                               |
|----------------------------------------|--------------------------|----------------------------------------------|
| Coleta de Confiabilidade (M1)      | Analistas de Qualidade   | Dias 1 a 3 (Execução do Teste de Uptime)           |
| Coleta de Confiabilidade (M2, M4)          | Avaliadores Técnicos     | Dia 2 (Execução do Teste de Carga e de Teste de Erros)          |
| Coleta de Confiabilidade (M3)          | Analistas de Qualidade   | Dia 3 (Análise de Logs/Histórico)         |
| Coleta de Portabilidade (M1, M2)       | Avaliadores Técnicos     | Dia 3 (Testes de Compatibilidade e Responsividade) |
| Consolidação dos Dados Brutos          | Analistas de Qualidade   | Dia 3                                       |
| Análise e Julgamento dos Resultados    | Todos                    | Dia 4                                       |
| Elaboração do Relatório da Fase 3      | Todos  | Dia 5                                        |


### 4. Fontes de Evidência e Rastreabilidade

A rastreabilidade é crucial para garantir a validade e a auditabilidade da avaliação.

| Fonte de Evidência                     | Local/Ferramenta                                          | Uso                                                                 | Avaliação Esperada                                                  |
|----------------------------------------|------------------------------------------------------------|---------------------------------------------------------------------|--------------------------------------------------------------------|
| Definição da Avaliação (Fase 2)        | Documento GQM (Seção 1)                                    | Roteiro formal que define o que e como medir.                      | O plano de coleta deve ser 100% fiel ao GQM da Fase 2.             |
| Dados Brutos Coletados                 | Planilha de Coleta de Dados                                | Armazenamento dos resultados numéricos e qualitativos (ex: contagem de inconsistências, percentuais de uptime). | Garante a auditabilidade e a base para o julgamento.               |
| Relatórios de Ferramentas              | Logs de Teste de Carga, Relatórios de Uptime, Screenshots de Inconsistências | Evidências primárias da execução dos testes.                       | Valida a execução do método e fornece dados brutos.                |
| Relatório Final da Fase 3              | Documento desta Fase                                       | Consolidação do Plano de Avaliação e preparação para a Fase 4 (Execução). | Deve referenciar todas as fontes de evidência e o GQM.             |

### 5. Registro e Armazenamento das Evidências

A documentação das evidências utilizadas na avaliação é fundamental para garantir rastreabilidade e facilitar a montagem da entrega final no GitHub Pages. Para isso, foi definido um fluxo centralizado para o armazenamento de dados, capturas de tela e vídeos produzidos durante a execução das métricas.

#### 5.1 Armazenamento dos Dados e Capturas de Tela

Os dados coletados durante a execução das métricas — incluindo valores numéricos, incidentes observados e anotações qualitativas — serão concentrados em um documento compartilhado. Esse mesmo arquivo também será utilizado para armazenar capturas de tela relevantes para as análises.

| Tipo de Evidência | Local de Armazenamento | Descrição do Uso |
|-------------------|------------------------|------------------|
| Dados numéricos, medições e observações | Documento compartilhado no Word Online | Registro contínuo dos dados brutos coletados, servindo como base para a análise e para a composição da entrega da Fase 4. |
| Capturas de tela (falhas, erros, inconsistências) | Documento compartilhado no Word Online | Armazenamento visual das evidências encontradas durante a execução das métricas. |

**Documento compartilhado:**  
[Link Docs](https://unbbr-my.sharepoint.com/:w:/g/personal/221037975_aluno_unb_br/EQaMnxEFQ0xNr9om1JMM5qcB_tgKDlwD1MvL30p7NcQyuQ?e=hA52o8)

#### 5.2 Armazenamento dos Vídeos dos Testes

Para cada métrica será gravado um vídeo curto demonstrando o procedimento de coleta, garantindo transparência e verificabilidade do processo. As gravações serão feitas utilizando o OBS Studio.

| Tipo de Evidência | Método de Produção | Local de Armazenamento | Descrição |
|-------------------|---------------------|--------------------------|-----------|
| Vídeos da execução das métricas | Gravação via OBS Studio | Drive compartilhado do grupo | Registro audiovisual da execução dos testes, permitindo revalidação e consulta posterior. |

**Pasta no Drive:**  
[Link Drive](https://drive.google.com/drive/u/2/folders/1EvH_bwVREh9tQuWpEAW8DweIy_RwK5xP)

### 5.3 Organização e Nomeação dos Arquivos

Para manter consistência e facilitar a integração com a página final, os arquivos seguirão o padrão de nomeação:

 ```
    <métrica>_<tipo_de_evidência>_<data>
    ex: M2_erro500_video_2025-11-20
    ex: M1_uptime_print_2025-11-19
 ```


### Histórico de Versões

| Versão | Descrição | Responsável | Data  | Revisor(es) | Detalhes da Revisão | Data da revisão |
| :----: | --------- | --------- | :--------------: | ----------- | :-------------: | :-------------: |
| `1.0` | documentação geral | [Maria Clara](https://github.com/alvezclari) | 17/11/2025|   |  |  |
| `2.0` | adicionando tópicos finais | [Natália De Morais](https://github.com/Natyrodrigues) | 18/11/2025|   |  |  |

