# Análises e Scripts — R'PIAS

## Sobre este Diretório

Este diretório armazena os scripts e notebooks de análise produzidos pelos projetos da R'PIAS. O objetivo é garantir **reprodutibilidade**, **transparência** e **reuso** das análises.

---

## Estrutura Recomendada

```
analises/
├── <SIGLA-PROJETO>/          # Uma pasta por projeto
│   ├── README.md             # Descreve as análises do projeto
│   ├── AAAA-descricao.R      # Scripts R individuais
│   ├── AAAA-descricao.Rmd    # RMarkdown com análise narrativa
│   └── AAAA-descricao.qmd    # Quarto document (alternativa ao Rmd)
└── comum/                    # Funções e scripts reutilizáveis pela rede
    └── funcoes_uteis.R
```

---

## Convenções de Nomenclatura

- Formato: `AAAA-descricao-curta.R` (ou `.Rmd`, `.qmd`, `.py`)
- Use apenas letras minúsculas, números e hífens (sem espaços ou acentos).
- Exemplos: `2025-analise-diversidade-especies.R`, `2025-mapa-uso-solo.qmd`

---

## Requisitos para Scripts

Todo script ou notebook depositado aqui deve conter no cabeçalho:

```r
# =============================================================================
# Título: <Título descritivo da análise>
# Projeto: <Sigla do projeto>
# Autor(a): <Nome> (@github)
# Data: <AAAA-MM-DD>
# Versão: <número>
# Descrição:
#   <Breve descrição do que a análise faz, quais dados usa, e o que produz>
# Dependências:
#   - R versão X.X.X ou superior
#   - Pacotes: tidyverse, ggplot2, ... (lista de pacotes)
# Dados de entrada:
#   - dados/brutos/<arquivo>.csv
# Dados de saída / figuras:
#   - relatorios/figuras/<arquivo>.png
# =============================================================================
```

---

## Gerenciamento de Pacotes R

Para garantir reprodutibilidade, use o pacote **`renv`** para registrar as versões de pacotes utilizadas em cada projeto.

```r
# Instalar renv (uma vez por máquina)
install.packages("renv")

# Inicializar renv no projeto
renv::init()

# Registrar pacotes utilizados
renv::snapshot()
```

O arquivo `renv.lock` gerado deve ser commitado junto com os scripts.

---

## Boas Práticas

1. **Caminhos relativos:** Use caminhos relativos à raiz do repositório (ex.: `../dados/brutos/arquivo.csv`), nunca caminhos absolutos.
2. **Semente aleatória:** Sempre defina `set.seed()` em análises que envolvem aleatoriedade.
3. **Comentários:** Comente o código de forma que outro pesquisador possa entender sem conhecimento prévio.
4. **Modularidade:** Separe etapas distintas (limpeza, análise, visualização) em scripts separados ou seções bem demarcadas.
5. **Não commit objetos grandes:** Não commite arquivos `.RData` ou `.rds` grandes — prefira recriar a partir dos scripts.
6. **Teste seu código:** Verifique se o script roda do zero em uma sessão R limpa antes de commitar.

---

## Linguagens e Ferramentas Suportadas

| Linguagem | Extensão | Uso principal |
|---|---|---|
| R | `.R`, `.Rmd`, `.qmd` | Análise estatística, visualização, relatórios |
| Python | `.py`, `.ipynb` | Machine learning, processamento de imagens, APIs |
| Bash | `.sh` | Automação, processamento em lote |

---

## Contribuindo com Análises

1. Crie ou use a pasta do seu projeto em `analises/<SIGLA-PROJETO>/`.
2. Siga as convenções de nomenclatura e o template de cabeçalho.
3. Documente dependências com `renv` (R) ou `requirements.txt` / `environment.yml` (Python).
4. Abra um Pull Request para revisão pelo supervisor antes de fazer merge na branch principal.

---

## Contato

Dúvidas sobre análises: abra uma *Issue* no repositório ou contate [@DSNogueira](https://github.com/DSNogueira).
