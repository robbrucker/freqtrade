- Follow everything in [Docker quickstart](docs/docker_quickstart.md)

- Check current BTC pairs on binance.us, edit `config.json`, list `pair_whitelist` to coincide with pairs on binance 

- Edit `config.json`, if following instructions from docker-quickstart, add: `"db_url"` key, the val is in `docker-compose.yml` --db-url
# Enter docker bash
`docker-compose exec freqtrade /bin/bash`


# Download some test data

`freqtrade download-data --pairs VET/BTC --exchange binanceus --days 10`


# Run a backfill test:

`freqtrade backtesting --config user_data/config.json --strategy minimal --timerange 20210301-20210325`