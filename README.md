# 🌱 Uso e Cobertura do Solo em Florianópolis (1985–2024)

**Análise espaço-temporal automatizada do uso e cobertura do solo no município de Florianópolis (SC)**

Este repositório apresenta um projeto de geoprocessamento e análise espacial que investiga como o uso e a cobertura do solo em Florianópolis evoluíram ao longo de 40 anos, utilizando dados oficiais do **MapBiomas** e automação em **Python**.

O foco está na **análise intraurbana por distritos administrativos**, combinando consistência espacial, eficiência computacional e visualização temporal.

---

## 🧭 Motivação

A paisagem urbana é resultado direto da interação entre sociedade e natureza ao longo do tempo. Entender **onde**, **como** e **quando** essas transformações ocorrem é essencial para:

- Planejamento urbano  
- Gestão ambiental  
- Formulação de políticas públicas  
- Comunicação científica e territorial  

Este projeto parte da seguinte pergunta:

> **Como a paisagem do município de Florianópolis se transformou entre 1985 e 2024?**

---

## 🎯 Objetivos

- Analisar a evolução do uso e cobertura do solo em Florianópolis  
- Comparar dinâmicas espaciais entre distritos administrativos  
- Garantir consistência espacial na manipulação de dados raster  
- Automatizar a produção de mapas, tabelas e visualizações temporais  
- Traduzir dados complexos em produtos visuais acessíveis  

---

## 🗺️ Área de estudo

- **Município:** Florianópolis – SC, Brasil  
- **Unidade de análise:** Distritos administrativos  
- **Fonte dos limites:** Prefeitura Municipal de Florianópolis

---

## 📦 Dados utilizados

### MapBiomas – Uso e Cobertura do Solo

- Coleção oficial (Coleção 10)  
- Séries anuais: **1985–2024**  
- Resolução espacial: **30 × 30 metros**

---

## ⚙️ Metodologia (resumo)

1. Recorte espacial do raster nacional utilizando os distritos como máscara  
2. Aplicação de buffer de 50 m para evitar pixels nulos nas bordas  
3. Reprojeção dos rasters para SIRGAS 2000 / UTM zona 22S (EPSG:31982)  
4. Vetorização anual dos rasters de uso do solo  
5. Armazenamento estruturado em GeoPackage (.gpkg)  
6. Validação espacial
7. Join com a legenda oficial do MapBiomas (classes, níveis e cores)  
8. Automação cartográfica para geração de mapas, tabelas e GIFs  

---

## 🧪 Tecnologias e ferramentas

- Python  
- GeoPandas  
- Rasterio  
- NumPy  
- Pandas  
- Matplotlib  
- Shapely  
- GDAL  
- QGIS (apoio exploratório)

## 📊 Resultados

- Mapas anuais de uso e cobertura do solo (1985–2024)  
- Tabelas de área por classe, ano e distrito  
- GIFs animados mostrando a evolução temporal de cada um dos **18 distritos**  
- Base vetorial consolidada em GeoPackage  

Esses produtos permitem análises quantitativas e leitura visual rápida das transformações territoriais.

---

## 📁 Estrutura do repositório
```text
├── data/
│   ├── raw/         
│   ├── processed/     
├── notebooks/
│   ├── 01 - Extração dos Rasters.ipynb
│   ├── 02 - ReprojetaRasters.ipynb
│   ├── 03 - Vetorização e Salvamento dos Dados.ipynb
│   ├── 04 - Verificação Area.ipynb
│   ├── 05 - Camadas para Tabela.ipynb
│   └── 06 - Geração de Mapas.ipynb
│   └── 07 - Gerar GIFS.ipynb
├── README.md

---

## ⚠️ Limitações

- Resolução espacial de 30 m pode suavizar mudanças muito localizadas

- Possíveis incertezas temáticas da classificação MapBiomas

- Não inclui variáveis socioeconômicas ou legais

## 🔮 Próximos passos

- Integração com dados demográficos e censitários

- Análise de conformidade com o Plano Diretor

- Estudos de fragmentação e conectividade florestal

- Dashboards interativos (Streamlit, Power BI, etc.)

- Expansão para outros municípios

## 📚 Referências

MapBiomas Brasil

Prefeitura Municipal de Florianópolis – Geoportal

## 👤 Autor

Theo G. Miqueluzzi
Geografia · Geoprocessamento · Análise Espacial
Florianópolis – SC
