# App Store Review Scrapper

[![License: MIT](https://img.shields.io/github/license/aerodiduch/review-scrapper)](LICENSE) ![Python](https://img.shields.io/badge/python-3776AB?logo=python&logoColor=white)

[Español](README.es.md)

A Python script that downloads the reviews of an app from Apple's App Store and saves them to a CSV, ready for analysis.

## Install

```sh
git clone https://github.com/aerodiduch/review-scrapper
cd review-scrapper
pip install -r requirements.txt
```

## Usage

1. Open `main.py` and, in the last lines, fill in the app's country, name and id. All three are in the app's App Store link. For Slack, `https://apps.apple.com/us/app/slack/id618783545` gives:

   ```python
   app = get_reviews(country='us', app_name='slack', app_id=618783545)
   ```

   Long names with dashes, like `my-super-long-app-name`, are fine.
2. Run it:

   ```sh
   python main.py
   ```

   The reviews end up in `data.csv`, in the same folder.

## How it works

It fetches the reviews with [app-store-scraper](https://pypi.org/project/app-store-scraper/) and writes the CSV with pandas. The dependencies are pinned to the versions from December 2022.

## License

MIT, see [LICENSE](LICENSE).
