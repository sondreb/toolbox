# toolbox
Toolbox for useful packages, hints, scripts, snippets and more

# Code Snippets

[sondreb's gists](https://gist.github.com/sondreb)

# Node Utilities

Change screen [brightness](https://github.com/kevva/brightness-cli):
```
npm install -g brightness-cli
```

Internet [speed test](https://github.com/sindresorhus/speed-test):
```
npm install -g speed-test
```

# Docker

The "docker" folder contains some useful compose configurations.

## Database

This compose template contains MongoDB and Microsoft SQL Server instances. You must create an "docker.env" file with an SA password for the MSSQL instance:

```
SA_PASSWORD=ThisIsYourImportantPassword!23
```

The usage of this template is to run database engines that can be used during development and testing without poluting your local OS.

Navigate into the [docker/database](docker/database) folder and run:

```
sudo docker-compose up -d
```

And when you are done, you can do:

```
sudo docker-compose down
```

This will not delete the persistent volumes.

After you have started the database engines, you can use MongoDB Compass to look at the Mongo databases and Azure Data Studio to look at the MSSQL databases.

https://www.mongodb.com/try/download/compass

https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio

## License

MIT © [Sondre Bjellås](http://sondreb.com)