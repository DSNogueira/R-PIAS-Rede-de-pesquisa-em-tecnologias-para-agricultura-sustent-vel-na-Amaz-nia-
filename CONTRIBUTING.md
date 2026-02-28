# Guia de Contribuição — R'PIAS

Bem-vindo(a) à rede R'PIAS! Este guia descreve como membros da rede e colaboradores externos podem contribuir com este repositório.

---

## Quem Pode Contribuir

- **Pesquisadores da rede:** têm acesso para criar branches e abrir Pull Requests diretamente neste repositório.
- **Colaboradores externos:** podem fazer um *fork* do repositório, contribuir em sua cópia e abrir um Pull Request.
- **Parceiros institucionais:** entre em contato com a coordenação para definir a forma de colaboração mais adequada.

---

## O Que Você Pode Contribuir

| Tipo de Contribuição | Onde Depositar |
|---|---|
| Novo projeto de pesquisa | `projetos/<ano>-<sigla>-<titulo>/` + atualizar `projetos/PROJETOS_ATIVOS.md` |
| Dados de campo ou processados | `dados/brutos/` ou `dados/processados/` + metadados em `dados/metadados/` |
| Scripts e análises | `analises/<sigla-projeto>/` |
| Relatório técnico | `relatorios/tecnicos/` |
| Artigo (preprint/rascunho) | `relatorios/artigos/` |
| Material de comunicação | `relatorios/comunicacao/` |
| Documentação geral | `docs/` |
| Correção de erros | Qualquer diretório relevante |

---

## Fluxo de Trabalho

### 1. Configure seu ambiente

```bash
# Clone o repositório (membros da rede)
git clone https://github.com/DSNogueira/R-PIAS-Rede-de-pesquisa-em-tecnologias-para-agricultura-sustent-vel-na-Amaz-nia-.git
cd R-PIAS-Rede-de-pesquisa-em-tecnologias-para-agricultura-sustent-vel-na-Amaz-nia-

# OU: faça um fork e clone o seu fork (colaboradores externos)
```

### 2. Crie uma branch para sua contribuição

```bash
git checkout -b <tipo>/<descricao-curta>
```

Exemplos:
- `dados/2025-SAF-inventario`
- `analise/2025-ILPF-produtividade`
- `docs/atualizar-parceiros`

### 3. Faça suas alterações

Siga as convenções de cada diretório (veja os `README.md` em `dados/`, `analises/`, `relatorios/` e `projetos/`).

### 4. Commit com mensagem descritiva

```bash
git add .
git commit -m "tipo: descrição breve (projeto)"
```

**Prefixos de commit:**
- `dados:` — dados novos ou atualizados
- `analise:` — scripts e análises
- `docs:` — documentação
- `relatorio:` — relatórios e artigos
- `projeto:` — proposta ou atualização de projeto
- `fix:` — correção de erro

### 5. Abra um Pull Request

```bash
git push origin <sua-branch>
```

No GitHub, abra um Pull Request da sua branch para `main`. Descreva:
- O que foi adicionado/modificado
- A qual projeto pertence
- Se há revisão pendente de supervisor

### 6. Revisão e merge

O(a) supervisor(a) ou coordenador(a) da linha de pesquisa revisará e fará o merge. Pode ser solicitado ajustes antes do merge.

---

## Padrões de Qualidade

### Dados
- Siga a política em [`dados/README.md`](dados/README.md).
- Todo dataset deve ter arquivo de metadados correspondente.
- Dados brutos nunca devem ser editados.

### Análises
- Siga as convenções em [`analises/README.md`](analises/README.md).
- Todo script deve ter cabeçalho documentado.
- Verifique que o script roda em sessão limpa antes de commitar.

### Documentação
- Use Markdown.
- Mantenha o estilo e nível de detalhe dos documentos existentes.
- Textos em Português (BR), salvo materiais destinados a publicação internacional.

---

## Comunicação e Dúvidas

- **Issues no GitHub:** use para reportar erros, propor melhorias ou tirar dúvidas.
- **Pull Requests:** use para submeter contribuições concretas.
- **Coordenação:** [@DSNogueira](https://github.com/DSNogueira)

---

## Código de Conduta

A R'PIAS é um espaço colaborativo e respeitoso. Esperamos que todos os contribuidores:

- Tratem os demais membros com respeito e inclusão;
- Reconheçam as contribuições de colegas adequadamente (autoria, agradecimentos);
- Sejam transparentes sobre limitações e incertezas nos dados e análises;
- Reportem problemas éticos ou de conduta à coordenação.

---

## Agradecimentos

Obrigado(a) por contribuir com a R'PIAS! Sua participação é fundamental para construirmos coletivamente uma agricultura mais sustentável na Amazônia. 🌿
