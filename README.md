# Desigualdade Educacional por Raça em Alagoas e no Brasil

Análise exploratória dos microdados do Censo Escolar 2023 (INEP),
investigando a relação entre raça/cor e acesso à infraestrutura
educacional no Brasil e em Alagoas.

## Principais achados

- Alagoas tem **82,1%** de alunos negros+pardos, contra 55% da média nacional
- Escolas com maioria indígena têm apenas **7% com laboratório de informática**
  contra 38% das escolas de maioria branca (Brasil)
- Na zona rural de Alagoas, apenas **10% das escolas têm biblioteca**
- Os municípios **Jundiá e Porto de Pedras** concentram a maior desigualdade
  racial×internet do estado
- A desigualdade opera em camadas: nacional, geográfica e estrutural (rede privada)

## Estrutura do projeto

```
desigualdade-educacional/
├── notebooks/
│   ├── 01_exploracao.ipynb        # limpeza e preparação
│   ├── 02_analise_racial.ipynb    # análise nacional por raça
│   ├── 03_alagoas.ipynb           # foco em Alagoas
│   ├── 04_mapa.ipynb      # mapas municipais
│   └── 05_estatistica.ipynb       # correlações e regressão
├── outputs/                        # gráficos gerados
├── data/
│   ├── raw/                        # dados brutos (não versionados)
│   └── processed/                  # dados processados (não versionados)
└── README.md
```

## Como reproduzir

1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/desigualdade-educacional.git
```

2. Instale as dependências
```bash
pip install pandas numpy matplotlib seaborn geopandas scipy plotly jupyter openpyxl
```

3. Baixe os dados do INEP
   - Acesse: https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/censo-escolar
   - Baixe os **Microdados do Censo Escolar 2023**
   - Coloque `microdados_ed_basica_2023.csv` em `data/raw/`
   - Baixe o shapefile de Alagoas do IBGE e coloque em `data/raw/shapes/AL_municipios/`

4. Execute os notebooks em ordem (01 → 05)

## Tecnologias

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.x-green)
![GeoPandas](https://img.shields.io/badge/GeoPandas-mapping-orange)

## Fonte dos dados

- **INEP** — Microdados do Censo Escolar 2023
- **IBGE** — Malha municipal de Alagoas 2023
