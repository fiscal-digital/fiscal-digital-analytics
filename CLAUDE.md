# Fiscal Digital — Analytics

## Hierarquia de contexto (lê PRIMEIRO)

Antes de qualquer trabalho aqui, **abrir e ler [`../fiscal-digital/CLAUDE.md`](../fiscal-digital/CLAUDE.md)**.

Esse é o documento mestre do projeto. Princípios inegociáveis, governança
open source, contrato com brand pack — tudo lá. **Não duplicar conteúdo aqui.**

---

## Escopo local

Este repo hospeda análises exploratórias, relatórios trimestrais e exports
de dados derivados dos alertas e do pipeline do Fiscal Digital.

### Stack

- Python 3.12+
- Jupyter / JupyterLab para notebooks
- pandas, polars (datasets grandes)
- Quarto para relatórios em HTML/PDF
- GitHub Pages para publicação dos relatórios

### Estrutura de diretórios

```
notebooks/   Análises exploratórias reprodutíveis
reports/     Relatórios formatados (Quarto)
data/        (gitignored) datasets locais
```

### Convenções específicas

- **Reprodutibilidade obrigatória:** todo notebook tem `requirements.txt`
  ou `pyproject.toml` no mesmo diretório
- **Dados:** nunca commitar datasets grandes — usar Git LFS ou DVC
- **Relatórios:** sempre incluir nota metodológica + fonte dos dados +
  período + recortes aplicados
- **Voz dos relatórios:** factual, conforme `fiscal-digital-web/brand/voice-tone.md`
  — termos da `glossary.json#avoid` proibidos

### Licença CC-BY 4.0 (não MIT)

Este repo é o ÚNICO `fiscal-digital-*` com licença CC-BY 4.0. Razão:
contém majoritariamente conteúdo (relatórios, datasets, análises), não
software. Padrão Open Knowledge para projetos de dados abertos.

### Brand pack

Quando relatórios incluírem visualizações, usar tokens de cor de
`fiscal-digital-web/brand/colors.json`. Em build-time:

```python
import json, urllib.request
url = "https://raw.githubusercontent.com/fiscal-digital/fiscal-digital-web/main/brand/colors.json"
brand = json.loads(urllib.request.urlopen(url).read())
deep_teal = brand["colors"]["deepTeal"]["hex"]  # "#0D4F4A"
```

Mapeamento `riskScore → cor` segue `colors.json#risk` — único source of truth.
