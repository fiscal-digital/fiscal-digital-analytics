<p align="center">
  <img src="https://raw.githubusercontent.com/fiscal-digital/fiscal-digital-web/main/brand/logo/symbol.svg" width="96" alt="Fiscal Digital" />
</p>

# Fiscal Digital — Analytics

**Notebooks, relatórios e exports CSV — análises reproduzíveis do Fiscal Digital.**

[fiscaldigital.org](https://fiscaldigital.org) · [@FiscalDigitalBR](https://x.com/FiscalDigitalBR)

---

## 🇧🇷 Português

Este repo hospeda análises exploratórias, relatórios trimestrais e *exports* CSV/Parquet derivados dos alertas e dados coletados pelo Fiscal Digital.

### Stack

Python 3.12+ · Jupyter / JupyterLab · pandas / polars · Quarto (relatórios) · GitHub Pages para publicação.

### Estrutura

```
notebooks/   Análises exploratórias e cadernos reprodutíveis
reports/     Relatórios formatados (Quarto / HTML / PDF)
data/        (gitignored) datasets locais — usar Git LFS ou DVC para grandes
```

### Princípios

- **Reprodutibilidade obrigatória:** todo notebook tem `requirements.txt` ou `pyproject.toml` no mesmo diretório
- **Datasets grandes nunca commitados:** usar Git LFS ou referência via DVC
- **Nota metodológica em cada relatório:** fonte dos dados, período, recortes
- **Voz factual:** relatórios seguem [`fiscal-digital-web/brand/voice-tone.md`](https://github.com/fiscal-digital/fiscal-digital-web/blob/main/brand/voice-tone.md)

### Status

🚧 **Em desenvolvimento.** Primeiros notebooks descreverão padrões da gestão Adiló (Caxias do Sul, 2021–presente) após o pipeline da engine gerar volume relevante de alertas.

### Licença

Conteúdo, datasets e relatórios sob **CC-BY 4.0** — uso livre, com crédito.

Esta licença é deliberadamente diferente da do código (MIT em outros repos do projeto), seguindo o padrão da Open Knowledge para projetos de dados abertos.

Ver [LICENSE](LICENSE).

---

## 🇺🇸 English

Notebooks, quarterly reports, and CSV/Parquet exports derived from Fiscal Digital alerts and collected data.

Stack: Python 3.12+, Jupyter, pandas/polars, Quarto.

Status: under development.

License: **CC-BY 4.0** — free use with attribution. This is deliberately different from the code repos (MIT), following the Open Knowledge convention for open data projects.

---

*Sobre os ombros de [Serenata de Amor](https://serenata.ai) e [Querido Diário](https://queridodiario.ok.org.br) (OKFN Brasil).*
