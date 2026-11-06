# Mulheres no Brasil (IBGE)

Parte individual do Projeto Integrado Python/Matemática "Números que Falam", **indicador 4**.

**Aluno:** Thales Alves Gomes

Dashboard em Streamlit sobre a população feminina em cada município do Brasil, segundo o Censo 2010 e o Censo 2022:
percentual de mulheres por faixa etária, domicílios chefiados por mulheres e mulheres por cor ou raça.
Mostra média, mediana, moda, quartis, IQR, amplitude, variância, desvio padrão e outliers (regra de 1,5 × IQR).

## Arquivos
- `app.py`: o dashboard (upload, filtros, indicadores, gráficos, notícias)
- `etl_mulheres.py`: baixa os dados do IBGE e gera a base tratada
- `dados/mulheres_municipios.csv`: base tratada (um registro por município, ano e situação urbana/rural)
- `analise_descritiva.md`: interpretação dos resultados
- `gerar_imagens.py` e `imagens/`: imagens ilustrativas da seção de notícias

## Como rodar
```
pip install -r requirements.txt
streamlit run app.py
```

A base tratada já vem pronta. Para gerar de novo a partir dos dados brutos, rode `python etl_mulheres.py`
(baixa cerca de 420 MB).

## Fonte
IBGE, Censo Demográfico 2010 e 2022, Agregados por Setores Censitários. Arquivos brutos obtidos pela cópia
em parquet do IPEA (pacote censobr).
