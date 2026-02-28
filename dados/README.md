# Gestão de Dados — R'PIAS

## Política de Dados da Rede

Este diretório armazena os dados coletados e utilizados nos projetos de pesquisa da R'PIAS. Todo dado depositado aqui deve seguir as convenções descritas neste documento.

---

## Estrutura de Pastas

```
dados/
├── brutos/          # Dados originais, exatamente como coletados (NUNCA editar)
├── processados/     # Dados após limpeza e transformações documentadas
├── externos/        # Dados de fontes externas (IBGE, INPE, etc.) com metadados de origem
├── geoespaciais/    # Arquivos GIS (Shapefile, GeoJSON, GeoTIFF)
└── metadados/       # Dicionários de variáveis e documentação de datasets
```

---

## Convenções de Nomenclatura

### Arquivos de dados

Formato: `AAAA-SIGLAPROJETO-descricao-versao.extensao`

Exemplos:
- `2025-SAF-inventario-especies-v1.csv`
- `2025-ILPF-dados-producao-parcela-v2.xlsx`
- `2025-SOLO-amostras-quimicas-v1.csv`

### Pastas de projeto dentro de `dados/`

Organize dados por projeto quando o volume justificar:

```
dados/brutos/
├── 2025-SAF/
│   ├── 2025-SAF-inventario-especies-v1.csv
│   └── 2025-SAF-dados-solo-v1.xlsx
└── 2025-ILPF/
    └── ...
```

---

## Obrigatoriedade de Metadados

**Todo arquivo de dados depositado neste repositório deve ter um arquivo de metadados correspondente** em `dados/metadados/`, com o mesmo nome e extensão `.md`.

### Exemplo de Metadados (`2025-SAF-inventario-especies-v1.md`)

```markdown
# Metadados: 2025-SAF-inventario-especies-v1.csv

| Campo | Informação |
|---|---|
| **Projeto** | SAF-2025 |
| **Responsável** | @usuario |
| **Data de coleta** | Janeiro–Março 2025 |
| **Área de estudo** | Município X, Estado Y (coordenadas: lat, lon) |
| **Método de coleta** | Inventário florestal em parcelas de 20x50m |
| **Número de registros** | 1.240 linhas |
| **Versão** | 1.0 |
| **Licença** | CC BY 4.0 |
| **Última atualização** | 2025-03-15 |

## Dicionário de Variáveis

| Variável | Tipo | Unidade | Descrição |
|---|---|---|---|
| parcela_id | texto | — | Identificador único da parcela |
| especie | texto | — | Nome científico da espécie |
| cap_cm | numérico | cm | Circunferência à altura do peito |
| altura_m | numérico | m | Altura total estimada |
| ...| | | |

## Observações
- (Anote qualquer particularidade sobre os dados, valores faltantes, etc.)
```

---

## Regras Gerais

1. **Nunca edite os dados brutos.** Se precisar corrigir um erro, crie uma nova versão em `dados/processados/` e documente a transformação.
2. **Versione os dados.** Incremente o número de versão (`v1`, `v2`, ...) ao fazer alterações significativas.
3. **Não commit arquivos grandes (>50 MB) diretamente.** Use Git LFS ou armazene externamente e documente o link de acesso nos metadados.
4. **Proteja dados sensíveis.** Dados com identificação de pessoas ou coordenadas precisas de comunidades devem ser anonimizados ou armazenados em repositório privado com acesso controlado.
5. **Cite a fonte.** Para dados externos, sempre inclua a referência completa e a URL de origem nos metadados.

---

## Formatos Aceitos

| Tipo de dado | Formato preferencial | Formato alternativo |
|---|---|---|
| Dados tabulares | CSV (UTF-8) | Excel (.xlsx) |
| Dados geoespaciais vetoriais | GeoJSON | Shapefile (.shp) |
| Dados geoespaciais raster | GeoTIFF | ASC/NetCDF |
| Imagens de campo | JPEG / PNG | |
| Documentos | PDF / Markdown | Word (.docx) |

---

## Acesso e Licenciamento

- Dados publicados neste repositório são disponibilizados sob **[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)** salvo indicação contrária nos metadados.
- Dados com restrições de acesso devem ser indicados nos metadados e não devem ser commitados neste repositório público.

---

## Contato

Dúvidas sobre organização de dados: abra uma *Issue* no repositório ou contate [@DSNogueira](https://github.com/DSNogueira).
