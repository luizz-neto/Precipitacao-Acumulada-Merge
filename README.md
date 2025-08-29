# 🌧️ Processamento de Precipitação Acumulada (CPTEC/INPE)

Este repositório contém um conjunto de scripts em **Python** para o processamento e visualização de dados de **precipitação acumulada** obtidos a partir de arquivos **GRIB2** disponibilizados pelo **CPTEC/INPE**.  

O fluxo do código inclui:  
- 📥 **Download automático** dos arquivos `.grib2` (via scraping)  
- 🗂️ **Processamento e soma acumulada** da variável de precipitação  
- 💾 **Exportação em NetCDF (.nc)**  
- 🗺️ **Geração de mapas temáticos** em `.png` com delimitação do Brasil  

---

## ⚙️ Etapas principais do script

1. **Download dos dados**  
   - Acesso ao site do CPTEC/INPE  
   - Coleta automática dos arquivos `.grib2`  

2. **Processamento da precipitação**  
   - Leitura apenas das variáveis de precipitação (`prec`)  
   - Cálculo da soma acumulada ao longo do tempo  
   - Salvamento em formato **NetCDF (.nc)**  

3. **Visualização cartográfica**  
   - Projeção: `PlateCarree` (Cartopy)  
   - Colormap inspirado no **INMET**  
   - Inclusão de shapefile do Brasil para recorte  
   - Geração do mapa em `.png`  

---

## 📊 Arquivos de saída

| Arquivo                  | Descrição                                                   |
|---------------------------|-------------------------------------------------------------|
| `prec_acumulada.nc`      | Dados acumulados de precipitação em formato NetCDF           |
| `prec_acumulada_mapa.png`| Mapa temático da precipitação acumulada (região da América do Sul) |

---

## 🎯 Aplicações

- Estudos de **eventos hidrológicos extremos** (enchentes, secas)  
- Monitoramento **climatológico e meteorológico**  
- Análises em **modelagem hidrológica**  
- Apoio à **gestão de recursos hídricos**  

---

## 🛠️ Tecnologias utilizadas

- [Python 3.10+](https://www.python.org/)  
- [xarray](https://docs.xarray.dev/)  
- [numpy](https://numpy.org/)  
- [matplotlib](https://matplotlib.org/)  
- [cartopy](https://scitools.org.uk/cartopy/docs/latest/)  
- [geopandas](https://geopandas.org/)  
- [cfgrib](https://github.com/ecmwf/cfgrib)  

---
