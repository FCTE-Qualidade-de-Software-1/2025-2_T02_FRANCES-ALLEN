# Avaliação do Site Cebraspe — Fase 2

**Características analisadas:** Confiabilidade e Portabilidade  
**Base normativa:** ISO/IEC 25010 – SQuaRE  
**Produto:** Site do Cebraspe ([https://www.cebraspe.org.br/](https://www.cebraspe.org.br/))  
**Versão:** Atual (outubro de 2025)

---

## 1. Objetivos da Avaliação

| Característica | Objetivo |
|----------------|-----------|
| **Confiabilidade** | Avaliar a capacidade do site do Cebraspe de manter seu funcionamento correto e contínuo durante períodos de alta demanda, garantindo disponibilidade, tolerância a falhas e consistência de dados. |
| **Portabilidade** | Avaliar o grau em que o site pode ser utilizado em diferentes dispositivos, sistemas operacionais e navegadores, sem perda de funcionalidade ou usabilidade. |

---

## 2. Questões de Avaliação e Métricas

As **questões** orientam a investigação e as **métricas** quantificam o desempenho observado.  
Cada questão abaixo está associada a um ou mais **subatributos** da ISO/IEC 25010.

### 2.1 Confiabilidade

| Subcaracterística (ISO 25010) | Questão de Avaliação | Métricas |
|-------------------------------|----------------------|-----------|
| **Disponibilidade** | O site do Cebraspe permanece acessível continuamente, especialmente durante períodos críticos (ex.: abertura de inscrições)? | - Taxa de disponibilidade (% uptime): tempo total disponível ÷ tempo total observado × 100 <br> - Tempo médio de inatividade (MTBF): média de tempo entre falhas ou indisponibilidades <br> - Tempo de recuperação (MTTR): tempo médio até o restabelecimento após falha |
| **Tolerância a falhas** | O sistema mantém o funcionamento mesmo em caso de falhas parciais ou sobrecarga de acesso? | - Tempo de resposta sob carga (s) <br> - Taxa de erro (%): número de erros de servidor (HTTP 5xx) ÷ total de requisições |
| **Recuperabilidade** | O sistema consegue retornar ao estado operacional após falhas ou interrupções? | - Tempo de restabelecimento automático <br> - Integridade dos dados após falhas |
| **Maturidade** | O site apresenta falhas recorrentes ou instabilidades? | - Número de incidentes reportados por período <br> - Tempo médio entre incidentes (MTBI) |

---

### 2.2 Portabilidade

| Subcaracterística (ISO 25010) | Questão de Avaliação | Métricas |
|-------------------------------|----------------------|-----------|
| **Adaptabilidade** | O site se adapta automaticamente a diferentes tamanhos de tela (desktop, tablet, smartphone)? | - Taxa de conformidade de layout responsivo (%): páginas funcionais ÷ total de páginas testadas × 100 <br> - Pontuação de responsividade (via Lighthouse) |
| **Instalabilidade / Acessibilidade técnica** | O site é acessível de diferentes navegadores e sistemas operacionais sem necessidade de configurações adicionais? | - Compatibilidade entre navegadores (%): nº de navegadores em que o site funciona ÷ nº de navegadores testados <br> - Compatibilidade entre sistemas operacionais (%): nº de sistemas compatíveis ÷ nº de sistemas testados |
| **Substituibilidade / Tecnologias assistivas** | É possível acessar o site com tecnologias assistivas e diferentes interfaces (ex.: navegador mobile, leitor de tela)? | - Taxa de compatibilidade com leitores de tela (%) <br> - Pontuação de acessibilidade (Lighthouse / WAVE) |

---

## 3. Considerações Metodológicas

**Ferramentas Sugeridas:**

- Lighthouse (Chrome DevTools): avaliação automática de desempenho, acessibilidade, responsividade e compatibilidade  
- Pingdom / UptimeRobot: monitoramento de disponibilidade (uptime, tempo de resposta)  
- GTmetrix: análise de tempo de carregamento e estabilidade sob carga  
- BrowserStack: teste de compatibilidade entre navegadores e sistemas  
- WAVE / AXE: validação de acessibilidade  

**Amostra de Páginas Testadas:**

- Página inicial  
- Página de concursos em andamento  
- Página de detalhes de um concurso  
- Página institucional (“Sobre o Cebraspe”)  

**Período de Coleta:** 5 dias úteis (horários de pico e fora de pico)

---

## 4. Critérios de Aceitação

| Característica | Métrica Crítica | Valor de Referência | Nível de Aceitação |
|----------------|-----------------|------------------|------------------|
| **Confiabilidade** | Disponibilidade | ≥ 99,5% | Aceitável |
| **Confiabilidade** | Tempo médio de resposta | ≤ 3s | Aceitável |
| **Confiabilidade** | Taxa de erro | ≤ 1% | Aceitável |
| **Portabilidade** | Compatibilidade entre navegadores | ≥ 90% | Aceitável |
| **Portabilidade** | Pontuação Lighthouse (Mobile) | ≥ 80 | Aceitável |
| **Portabilidade** | Responsividade de layout | 100% das páginas principais | Aceitável |

---

## 5. Interpretação dos Resultados

- **Alta confiabilidade** será demonstrada se o site mantiver alta disponibilidade, baixo tempo de resposta e mínima ocorrência de falhas.  
- **Alta portabilidade** será observada se o site mantiver desempenho e aparência consistentes em diferentes plataformas e dispositivos.  
- Eventuais falhas (ex.: incompatibilidade com Safari iOS ou travamentos sob carga) deverão ser documentadas com **capturas de tela e logs** para subsidiar recomendações de melhoria.

---

## 6. Próximos Passos

- Consolidação dos resultados em relatório técnico (Fase 3)  
- Proposição de melhorias com base nas não conformidades observadas  
- Reavaliação futura após implementação das correções


## Histórico de Versões

| Versão | Descrição | Responsável | Data  | Revisor(es) | Detalhes da Revisão | Data da revisão |
| :----: | --------- | --------- | :--------------: | ----------- | :-------------: | :-------------: |
| `1.0` | documentação inicial e estrutura geral | [Natalia ](https://github.com/Natyrodrigues) | 
