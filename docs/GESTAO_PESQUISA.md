# Guia de Gestão e Supervisão de Pesquisas — R'PIAS

> Este documento orienta coordenadores, supervisores e orientadores na gestão das atividades de pesquisa da rede R'PIAS. Ele serve como referência para planejamento, acompanhamento, avaliação e comunicação de projetos e resultados.

---

## 1. Papel do Supervisor/Orientador na R'PIAS

O(a) **supervisor(a)/orientador(a)** na R'PIAS desempenha um papel central de liderança científica e gestão estratégica, com as seguintes responsabilidades:

### 1.1 Liderança Científica
- Definir e atualizar as perguntas de pesquisa prioritárias da rede.
- Garantir rigor metodológico e alinhamento com os objetivos da PIAS.
- Orientar pesquisadores em formação no desenvolvimento de projetos individuais.
- Promover a integração entre as diferentes linhas de pesquisa.

### 1.2 Gestão de Projetos
- Planejar cronogramas, marcos e entregas de cada projeto.
- Acompanhar o progresso e identificar riscos e gargalos.
- Facilitar a resolução de problemas metodológicos e logísticos.
- Garantir o cumprimento de prazos e obrigações com financiadores.

### 1.3 Desenvolvimento de Pessoas
- Orientar estudantes de graduação, mestrado e doutorado.
- Promover capacitações metodológicas (análise de dados, escrita científica, campo).
- Estimular a autonomia científica e o espírito crítico dos pesquisadores.
- Criar um ambiente colaborativo, inclusivo e psicologicamente seguro.

### 1.4 Comunicação e Articulação
- Representar a rede em fóruns científicos e de políticas públicas.
- Manter diálogo ativo com parceiros institucionais e financiadores.
- Coordenar a comunicação dos resultados para diferentes públicos.

---

## 2. Ciclo de Gestão de Pesquisa

```
  ┌─────────────────────────────────────────────────────┐
  │                                                     │
  ▼                                                     │
[1. Planejamento] → [2. Execução] → [3. Monitoramento] → [4. Avaliação] → [5. Comunicação]
                                                              │
                                                              └──→ [6. Revisão/Novo Ciclo]
```

### Fase 1 — Planejamento
- [ ] Identificar problemas de pesquisa prioritários (com participação dos parceiros).
- [ ] Elaborar proposta de projeto usando o [`TEMPLATE_PROJETO.md`](../projetos/TEMPLATE_PROJETO.md).
- [ ] Definir equipe, responsabilidades e cronograma.
- [ ] Identificar fontes de financiamento e submeter propostas.
- [ ] Registrar o projeto em [`PROJETOS_ATIVOS.md`](../projetos/PROJETOS_ATIVOS.md).
- [ ] Criar pasta do projeto em `projetos/<nome-do-projeto>/`.

### Fase 2 — Execução
- [ ] Conduzir coleta de dados conforme protocolo definido.
- [ ] Organizar dados em `dados/` seguindo as convenções documentadas.
- [ ] Desenvolver e documentar análises em `analises/`.
- [ ] Realizar reuniões de acompanhamento (veja seção 3).

### Fase 3 — Monitoramento
- [ ] Atualizar status do projeto mensalmente em `PROJETOS_ATIVOS.md`.
- [ ] Revisar indicadores de progresso em relação ao cronograma.
- [ ] Identificar desvios e acionar plano de contingência quando necessário.
- [ ] Registrar decisões e mudanças metodológicas no log do projeto.

### Fase 4 — Avaliação
- [ ] Verificar cumprimento dos objetivos e metas do projeto.
- [ ] Consolidar resultados e aprendizados.
- [ ] Realizar avaliação participativa com parceiros e beneficiários.
- [ ] Documentar lições aprendidas.

### Fase 5 — Comunicação
- [ ] Elaborar relatório técnico final em `relatorios/`.
- [ ] Submeter artigo(s) científico(s) a periódicos relevantes.
- [ ] Produzir materiais de divulgação para não-especialistas.
- [ ] Apresentar resultados em eventos científicos e de políticas públicas.

### Fase 6 — Revisão e Novo Ciclo
- [ ] Atualizar documentação da PIAS com novos conhecimentos.
- [ ] Refinar perguntas de pesquisa com base nos resultados.
- [ ] Planejar próximos projetos e captação de recursos.

---

## 3. Rotina de Reuniões

| Tipo | Frequência | Participantes | Objetivo |
|---|---|---|---|
| **Reunião de Orientação Individual** | Quinzenal | Supervisor + pesquisador(a) | Acompanhamento de progresso, resolução de dúvidas, planejamento |
| **Reunião de Grupo de Pesquisa** | Mensal | Toda a equipe da linha de pesquisa | Apresentação de resultados parciais, discussão metodológica |
| **Reunião da Rede** | Trimestral | Todos os membros da R'PIAS | Integração entre linhas, atualização estratégica, articulação |
| **Seminário Aberto** | Semestral | Membros + convidados externos | Apresentação de resultados, diálogo com parceiros e comunidade |

### Modelo de Pauta (Reunião de Orientação Individual)
1. Revisão das pendências da última reunião
2. Progresso desde o último encontro (coleta, análise, escrita)
3. Dificuldades e necessidades de apoio
4. Planejamento das próximas semanas
5. Datas, prazos e entregas

---

## 4. Gerenciamento de Projetos no Repositório

### Convenções de Nomenclatura

- **Pastas de projetos:** `projetos/<ANO>-<SIGLA>-<titulo-curto>/`  
  Exemplo: `projetos/2025-SAF-sistemas-agroflorestais-para-terra-firme/`

- **Arquivos de dados:** `dados/<tipo>/<ANO>-<projeto>-<descricao>.<ext>`  
  Exemplo: `dados/brutos/2025-SAF-inventario-especies.csv`

- **Scripts de análise:** `analises/<projeto>/<ANO>-<descricao>.R`  
  Exemplo: `analises/SAF/2025-analise-diversidade.R`

- **Relatórios:** `relatorios/<tipo>/<ANO>-<projeto>-<descricao>.md`  
  Exemplo: `relatorios/tecnicos/2025-SAF-relatorio-parcial.md`

### Fluxo de Trabalho Git

Para pesquisadores que utilizam o repositório:

```bash
# Clone o repositório
git clone https://github.com/DSNogueira/R-PIAS-Rede-de-pesquisa-em-tecnologias-para-agricultura-sustent-vel-na-Amaz-nia-.git

# Crie uma branch para seu projeto ou contribuição
git checkout -b <seu-nome>/<descricao-curta>

# Faça alterações, adicione e commite
git add .
git commit -m "tipo: descrição breve (projeto)"

# Envie para revisão
git push origin <sua-branch>
# Abra um Pull Request no GitHub para revisão pelo supervisor
```

**Prefixos de commit recomendados:**
- `dados:` — adição ou atualização de dados
- `analise:` — scripts e análises
- `docs:` — documentação
- `relatorio:` — relatórios e artigos
- `fix:` — correção de erros

---

## 5. Indicadores de Acompanhamento da Pesquisa

### Por Projeto
| Indicador | Como medir | Frequência |
|---|---|---|
| % de cumprimento do cronograma | Marcos concluídos / total de marcos planejados | Mensal |
| Volume de dados coletados | Registros / meta definida | Por campanha |
| Publicações submetidas | Contagem de submissões | Semestral |
| Publicações aceitas/publicadas | Contagem de publicações | Anual |

### Por Pesquisador(a)
| Indicador | Como medir | Frequência |
|---|---|---|
| Reuniões realizadas | Contagem | Mensal |
| Progresso da dissertação/tese | Capítulos/seções concluídas | Semestral |
| Participação em eventos | Apresentações/pôsteres | Anual |
| Contribuições ao repositório | Commits/pull requests | Mensal |

---

## 6. Gestão de Conflitos e Questões Éticas

- **Autoria:** Seguir os critérios da ICMJE (International Committee of Medical Journal Editors) para definição de autoria em publicações.
- **Dados de comunidades:** Garantir Consentimento Livre, Prévio e Informado (CLPI) e acordos de co-autoria ou uso de dados com comunidades parceiras.
- **Conflitos de interesse:** Declarar abertamente em publicações e reuniões.
- **Conflitos interpessoais:** Escalar para a Coordenação Geral com confidencialidade garantida.

---

## 7. Recursos e Ferramentas de Apoio

| Recurso | Uso | Link |
|---|---|---|
| GitHub | Controle de versão, colaboração | Este repositório |
| R / RStudio | Análise estatística e visualização | [r-project.org](https://www.r-project.org/) |
| QGIS | Análise geoespacial | [qgis.org](https://qgis.org/) |
| Zotero | Gestão de referências bibliográficas | [zotero.org](https://www.zotero.org/) |
| ODK / KoboToolbox | Coleta de dados em campo (mobile) | [kobotoolbox.org](https://www.kobotoolbox.org/) |

---

## 8. Dúvidas Frequentes

**Como registro um novo projeto?**  
Use o template em [`projetos/TEMPLATE_PROJETO.md`](../projetos/TEMPLATE_PROJETO.md), crie uma cópia em `projetos/<sua-pasta>/PROJETO.md` e adicione uma linha em `projetos/PROJETOS_ATIVOS.md`.

**Como organizo meus dados no repositório?**  
Consulte a política em [`dados/README.md`](../dados/README.md).

**Como preparo um script de análise para o repositório?**  
Consulte as diretrizes em [`analises/README.md`](../analises/README.md).

**Onde deposito meu relatório técnico ou artigo?**  
Consulte as instruções em [`relatorios/README.md`](../relatorios/README.md).
