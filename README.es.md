# App Store Review Scraper

[![License: MIT](https://img.shields.io/github/license/aerodiduch/review-scraper)](LICENSE) ![Python](https://img.shields.io/badge/python-3776AB?logo=python&logoColor=white)

[English](README.md)

Un script de Python que baja las reseñas de una app del App Store de Apple y las guarda en un CSV, listas para analizar.

## Instalación

```sh
git clone https://github.com/aerodiduch/review-scraper
cd review-scraper
pip install -r requirements.txt
```

## Uso

1. Abrí `main.py` y, en las últimas líneas, completá el país, el nombre y el id de la app. Los tres están en el link de la app en el App Store. Para Slack, `https://apps.apple.com/us/app/slack/id618783545` da:

   ```python
   app = get_reviews(country='us', app_name='slack', app_id=618783545)
   ```

   Los nombres largos con guiones, como `mi-nombre-de-app-larguisimo`, andan igual.
2. Correlo:

   ```sh
   python main.py
   ```

   Las reseñas quedan en `data.csv`, en la misma carpeta.

## Cómo funciona

Baja las reseñas con [app-store-scraper](https://pypi.org/project/app-store-scraper/) y escribe el CSV con pandas. Las dependencias están fijadas en las versiones de diciembre de 2022.

## Licencia

MIT, ver [LICENSE](LICENSE).
