# Wingspan Tournament Data

This repository [downloads, aggregates, and cleans](./download_and_clean_data.ipynb) data from [Wingspan Tournament Discord](https://discord.gg/ryUwcZZYC7) tournaments by making [API requests to Challonge](https://api.challonge.com/v1), the platform we use to run many of our tournaments. It then uses that [aggregated and cleaned data](https://raw.githubusercontent.com/GracklinOatBrant/wingspan-tournament-data/main/wingspan_tournaments.json) to create a [visualization](https://gracklinoatbrant.github.io/wingspan-tournament-data) where you can explore and compare distributions of scores.

## Development

To run the underlying data generation notebook, first [download Pipenv](https://pipenv.pypa.io), and get a [Challonge API key](https://challonge.com/settings/developer). Then do the following:

```sh
cp .env.example .env
# update .env with your API key
pipenv install
pipenv shell
jupyter notebook
```

To test out changes to the extremely janky visualization, you can do something like:

```sh
python -m http.server
# then open http://localhost:8000 and start modifying index.html
```

Ping me on Discord if you have any ideas for improvements!
