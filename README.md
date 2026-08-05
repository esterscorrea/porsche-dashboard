# Porsche Sales Intelligence Dashboard

Dashboard de análise de vendas com identidade visual inspirada na Porsche — filtros interativos, KPIs em tempo real e insights de negócio, tudo em um único arquivo HTML, sem backend e sem dependência de internet.

🔗 **Demo ao vivo:** `https://esterscorrea.github.io/porsche-dashboard/` *(ative o GitHub Pages para gerar este link — veja instruções abaixo)*

![status](https://img.shields.io/badge/status-pronto-c6a567) ![tipo](https://img.shields.io/badge/tipo-single--file-1a1a1a)

---

## O que o dashboard responde

- **Quais modelos vendem mais em cada cidade?**
- **Qual ano de modelo teve mais saída em cada período de venda?**
- **Onde estão os maiores focos de demanda, e qual modelo lidera lá?**

## Funcionalidades

- **4 filtros combináveis:** Modelo Porsche, Ano do Modelo, Cidade, Forma de Pagamento
- **KPIs dinâmicos:** vendas registradas, receita total, ticket médio, modelo líder e cidade líder — recalculados a cada filtro
- **6 visualizações:** vendas por linha de modelo, formas de pagamento, unidades por ano do modelo (com seletor de período), tendência mensal, ranking de cidades e volume por praça
- **Tabela de transações** detalhada e ordenável por data
- **100% offline:** Chart.js embutido no próprio arquivo — abre direto no navegador, sem servidor

## Como usar

Baixe o arquivo `index.html` e abra no navegador. Não precisa instalar nada.

```bash
git clone https://github.com/esterscorrea/porsche-dashboard.git
cd porsche-dashboard
open index.html   # ou dois cliques no arquivo
```

## Sobre os dados

Base de 100 registros de vendas, tratados a partir de dados originais com inconsistências (datas em formatos diferentes, textos com capitalização variada). 24 registros tinham datas originais inválidas (ex.: "31 de abril") — foram mantidos em todas as análises e excluídos apenas do gráfico de tendência temporal, que depende de data válida.

| Campo | Descrição |
|---|---|
| `porsche_model` | Modelo do veículo vendido |
| `model_year` | Ano do modelo |
| `sale_date` | Data da venda |
| `sale_price` | Valor da venda |
| `vehicle_mileage` | Quilometragem no momento da venda |
| `payment_method` | Forma de pagamento |
| `city` / `state` | Localização da venda |
| `delivery_status` | Status de entrega |

## Stack

- HTML / CSS / JavaScript puro
- [Chart.js](https://www.chartjs.org/) (embutido, sem CDN)
- Sem frameworks, sem build step

## Publicar com GitHub Pages

1. Vá em **Settings → Pages** neste repositório
2. Em **Branch**, selecione `main` e a pasta `/ (root)`
3. Salve — em 1–2 minutos o link fica disponível em `https://esterscorrea.github.io/porsche-dashboard/`

## Design

Paleta preto/carvão com dourado, tipografia Space Grotesk + Inter + IBM Plex Mono, e "gauges" circulares nos KPIs como elemento de assinatura visual, remetendo ao painel analógico dos veículos da marca.

---

*Projeto pessoal de análise de dados e visualização, sem vínculo oficial com a Porsche AG.*
