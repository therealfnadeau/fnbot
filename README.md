# uabot
Bot to generate data to UA

Needs 3 environment variables to function :

SEARCHTOKEN  => API key to search

UATOKEN      => API key to send events to UA

SCENARIOSURL => Url to the scenario JSON file to randomize

GO15VENDOREXPERIMENT=1
To use the vendor folder for the lib for analytics/search api

## On windows
```sh
set SEARCHTOKEN = value
set UATOKEN = value
set SCENARIOSURL = value
set GO15VENDOREXPERIMENT=1
go run main.go
```

## To trigger a Docker rebuild, push with `latest`tag
```sh
1. Commit your changes
# We need to use the -f option here because tag latest already exists
2. git tag -f -a latest -m "Rebuild reason here"
# Push changes to branch + push changes to tag, you will need to supply credentials twice.
3. git push && git push -f --tags
```