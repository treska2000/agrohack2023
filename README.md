# AgroHack 2023 — Agricultural Occupation Clustering

[![License](https://img.shields.io/badge/license-MIT-blue)](./LICENSE.md)
![Python](https://img.shields.io/badge/python-v3.11+-blue.svg)
![Docker](https://img.shields.io/badge/docker-🐋-blue.svg)

🏆 **Winning solution** of the annual [AgroTech Hackathon](https://rshbdigital.ru/agrocode-hack) by Rosselkhozbank & AgroCode Hub.

Clusters agricultural job titles based on resume data — groups semantically similar professions and produces an interactive visualization of detected clusters.

---

## Pipeline

1. **Scraping** — collect resumes from job search sites via BeautifulSoup
2. **Embeddings** — build text representations with [compress-fastText](https://github.com/avidale/compress-fasttext)
3. **Clustering** — k-means with Silhouette metric for optimal cluster selection
4. **Visualization** — interactive dashboard via [Plotly Dash](https://dash.gallery/)
5. **Deployment** — containerized with Docker

## Installation

```bash
# Clone the repo
git clone https://github.com/treska2000/agrohack2023.git
cd agrohack2023

# Build Docker image
docker build -t agrohack2023 .

# Run
docker run -p 8050:8050 agrohack2023
```

## Stack

`Python 3.11` `compress-fastText` `scikit-learn` `Plotly Dash` `BeautifulSoup` `Docker`

## Team

[@treska2000](https://github.com/treska2000) · 
[@annulet](https://github.com/annulet) · 
[@vlade89](https://github.com/vlade89)
