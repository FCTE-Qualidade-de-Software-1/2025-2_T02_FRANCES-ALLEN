# Fase 1 - Definição dos Requisitos de Avaliação


## 1. Propósito da Avaliação 
O propósito desta avaliação é analisar o site do CEBRASPE sob a ótica das características de qualidade de software selecionadas [Confiabilidade e Portabilidade], a fim de identificar como o sistema se comporta em relação a esses atributos, propor melhorias e verificar alinhamento com as necessidades dos usuários.

### 1.1 Produto e versão a ser analisada
- Nome do Produto: Site do CEBRASPE
- URL: https://www.cebraspe.org.br/
- Versão: Versão atual (setembro de  2025)

### 1.2 Requisitante e Partes Interessadas
- **Requisitante:** Professora Cristiane Ramos (disciplina FGA315)
- **Partes Interessadas:**
  - **Cebraspe (Fornecedor/Desenvolvedor/Operador):** Interessa-se pela eficiência operacional, satisfação do usuário e conformidade com padrões de qualidade. Necessita de feedback para melhorias contínuas e para garantir a estabilidade e acessibilidade do site.
  - **Candidatos a Concursos (Usuários Finais):** Necessitam de um site confiável, sempre disponível e acessível em diferentes dispositivos e navegadores para realizar inscrições, consultar editais e resultados. A portabilidade é fundamental para que possam acessar as informações de qualquer lugar e com qualquer dispositivo.
  - **Instituições Contratantes:** Esperam que o Cebraspe forneça uma plataforma robusta e confiável para a gestão de seus processos seletivos, garantindo a integridade e a segurança das informações.

- **Público-Alvo**
  - **Primário:** Candidatos a concursos públicos, estudantes interessados em processos
seletivos
  - **Secundário:** Instituições parceiras, imprensa, pesquisadores, público em geral
interessado em transparência pública

## 2. Tipo de Produto e Descrição do Software 

O site do CEBRASPE é um sistema de informação web que atua como um portal para divulgação de concursos públicos, avaliações educacionais, certificações e informações institucionais. 

### Seções Principais: 
- **Institucional:** Informações sobre a organização, o que fazem, notícias, ouvidoria, etc. 
- **Concursos:** Listagem de concursos (novos, inscrições abertas, em andamento, encerrados), com páginas de detalhes para cada um. 
- **Avaliações:** Detalhes sobre avaliações educacionais e de políticas públicas. 
- **Certificações:** Informações sobre processos de certificação de conhecimentos. 
- **Acesso à Universidade:** Conteúdo relacionado a vestibulares e outros processos seletivos para universidades.
- **Interfaces:** O site é acessado via navegador web, com interfaces de usuário projetadas para desktop e dispositivos móveis. 
- **Dependências:** O site depende de um servidor web e banco de dados para armazenar informações de concursos e outros conteúdos.

## 3. Modelo de Qualidade
Para esta avaliação, será utilizado o modelo de qualidade ISO/IEC 25010 (SQuaRE), que fornece um framework abrangente para a avaliação da qualidade de produtos de software. Este modelo será adaptado para focar nas características de confiabilidade e portabilidade, que são as características priorizadas para esta projeto.


## 4. Características de Qualidade de Software Avaliadas 
As características de qualidade de software escolhidas para esta avaliação, com base na norma ISO/IEC 25010 (SQuaRE), são: Confiabilidade e Portabilidade. 

- **Confiabilidade**  
  - Motivação: garantir que o sistema funcione corretamente em situações críticas, como períodos de alta demanda em inscrições de concursos. A confiança do candidato depende diretamente da disponibilidade e precisão das informações. Nesse sentido, priorizamos a confiabilidade para garantir que o site funcione de forma consistente e sem interrupções, especialmente em momentos de pico de acesso.

- **Portabilidade**  
  - Motivação: possibilitar que o site seja acessado em diferentes dispositivos e navegadores, atendendo candidatos que utilizam computadores, tablets ou celulares, sem comprometer a experiência ou a consistência das funcionalidades. A portabilidade garante que nenhum candidato seja excluído devido a limitações tecnológicas, promovendo a inclusão no acesso às informações e serviços do Cebraspe.

Os critérios de priorização adotados para a escolha foram:
- **Impacto no Usuário Final:** Ambas as características têm um impacto direto e significativo na experiência do usuário do site do Cebraspe. Um site não confiável (com falhas, indisponibilidade) ou não portátil (não acessível em diferentes dispositivos/navegadores) impede o usuário de realizar suas tarefas essenciais (inscrição, consulta de resultados).
- **Relevância para o Cebraspe:** A credibilidade e a abrangência do Cebraspe dependem diretamente da confiabilidade de seus sistemas e da capacidade de alcançar o maior número possível de candidatos, independentemente da tecnologia que utilizam. Falhas ou limitações de acesso podem prejudicar a imagem da instituição e a eficácia de seus processos seletivos.

### Priorização MoSCoW

Aplicação da técnica *MoSCoW* para reforçar a priorização:

| Categoria   | Característica de Qualidade | Justificativa |
|-------------|------------------------------|---------------|
| *Must have* | Confiabilidade | É de suma importância que o site esteja sempre disponível e funcione sem falhas, especialmente em períodos críticos de concursos. Falhas podem resultar em perda de credibilidade e prejuízos diretos aos usuários. |
| *Must have* | Portabilidade | É fundamental que o site seja acessível em qualquer dispositivo e navegador para garantir a inclusão no acesso às informações para todos os candidatos |
| *Should have* | Segurança | Não é o foco principal desta avaliação, porém é de alta importância para proteger dados e garantir a integridade dos processos. |
| *Should have* | Manutenibilidade | Facilita evolução e correção do sistema no longo prazo. |
| *Could have* | Eficiência de Desempenho | Um site rápido melhora a experiência, mas confiabilidade/portabilidade são mais críticas para esta avaliação. |
| *Could have* | Compatibilidade | Embora relacionada à portabilidade, já é contemplada em grande parte pelos requisitos de acessibilidade em diferentes dispositivos e navegadores. |



O objetivo da nossa avaliação é identificar pontos fortes e áreas de melhoria para otimizar o site do Cebraspe. A priorização de confiabilidade e portabilidade está diretamente alinhada a este propósito, pois a melhoria nessas características impactará diretamente a satisfação do usuário, a credibilidade da instituição e a eficiência dos processos seletivos.
 
## 5. Escopo, Profundidade e Objetos de Avaliação
Será avaliada a versão atual do site público do Cebraspe.  

A análise cobrirá: disponibilidade, tempo de resposta, integridade de dados e conformidade com padrões de segurança. Será focada na interface web e na experiência do usuário, utilizando como base
as páginas públicas disponíveis e a navegação através das principais funcionalidades do site.

Serão utilizadas ferramentas e técnicas de análise estática e dinâmica, bem como testes de compatibilidade e responsividade.

**Objetos de Avaliação:**
- Disponibilidade do site (tempo de atividade).
- Compatibilidade com diferentes navegadores (Chrome, Firefox, Safari).
- Responsividade em diferentes tamanhos de tela (desktop, tablet, smartphone).


## 6. ODS Relacionados
Esta avaliação se conecta aos seguintes **Objetivos de Desenvolvimento Sustentável (ODS):**

**ODS 4 – Educação de Qualidade**  
- **Meta 4.3**: Até 2030, assegurar igualdade de acesso para todos os homens e mulheres a educação técnica, profissional e superior de qualidade.  
- **Meta 4.4**: Aumentar substancialmente o número de jovens e adultos que tenham competências relevantes, inclusive técnicas e profissionais, para emprego, trabalho decente e empreendedorismo.  
- **Justificativa**: O Cebraspe realiza exames de acesso à universidade e certificações, sendo peça-chave no processo educacional. A confiabilidade e a acessibilidade do site garantem que estudantes e candidatos tenham acesso às informações e oportunidades educacionais de forma justa.  


**ODS 9 – Indústria, Inovação e Infraestrutura**  
- **Meta 9.1**: Desenvolver infraestrutura de qualidade, confiável, sustentável e resiliente, para apoiar o desenvolvimento econômico e o bem-estar humano.  
- **Meta 9.c**: Aumentar significativamente o acesso às tecnologias da informação e comunicação, visando o acesso universal e acessível à internet.  
- **Justificativa**: O site do Cebraspe constitui uma infraestrutura digital essencial para a realização de concursos e avaliações. Um sistema de qualidade assegura maior alcance e acessibilidade, ampliando o acesso às informações e fortalecendo a inovação em serviços públicos digitais.  



**ODS 16 – Paz, Justiça e Instituições Eficazes**  
- **Meta 16.6**: Desenvolver instituições eficazes, responsáveis e transparentes em todos os níveis.  
- **Meta 16.10**: Assegurar o acesso público à informação e proteger as liberdades fundamentais.  
- **Justificativa**: O Cebraspe atua em processos de seleção pública, sendo fundamental que seu site apresente confiabilidade, disponibilidade e segurança. Isso fortalece a transparência, a justiça e a confiança nas instituições responsáveis por concursos e certificações.

## Tabela de Contribuição 

|  Matrícula |  Nome  |  Contribuição (%) |
|-------------|------------------|---------------------|
| 222006632 | [Daniel Ferreira](https://github.com/DanielFsR) | 16,7 |
| 200017772 | [Fellipe Silva](https://github.com/fellipepcs) | 16,7 |
| 222006801 | [Henrique Carvalho](https://github.com/henriquecarv3) | 16,7 |
| 222006893 | [Kaio Macedo](https://github.com/bigkaio) | 16,7 |
| 221008329 | [Maria Clara](https://github.com/alvezclari) | 16,7 |
| 221037975 | [Natalia Rodrigues](https://github.com/Natyrodrigues) | 16,7 |


## Histórico de Versões

| Versão | Descrição | Responsável | Data  | Revisor(es) | Detalhes da Revisão | Data da revisão |
| :----: | --------- | --------- | :--------------: | ----------- | :-------------: | :-------------: |
| `1.0` | documentação inicial e estrutura geral | [Natalia ](https://github.com/Natyrodrigues) | 28/09/2025 | [Maria Clara](https://github.com/alvezclari)  | | 28/09/2025 |
| `1.1` | acrescenta informções em cada tópico de acordo com os critérios de avaliação | [Maria Clara ](https://github.com/alvezclari) | 28/09/2025 |  | | |
| `1.2` | acrescenta tabela de priorização | [Daniel Ferreira](https://github.com/DanielFsR) | 29/09/2025 | [Maria Clara](https://github.com/alvezclari) | | 29/09/2025|
| `1.3` | acrescenta tabela de contribuição | [Maria Clara](https://github.com/alvezclari) | 30/09/2025 |  | | |
