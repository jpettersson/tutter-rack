Work in progress!

Reference implementation of how to run the Github robot [Tutter](https://github.com/JHaals/tutter) as a [Rack](http://rack.github.io/) app.<br />It will be compatible with the Heroku Ruby buildpack and will run on [Dokku](https://github.com/progrium/dokku).

## Getting started

### Install dependencies
`bundle`

### Configure 

Take a look at `config/tutter.yaml` and the official [tutter docs](https://github.com/JHaals/tutter)

### Run 

`rackup config.ru`

### Deploy

Push to Heroku or Dokku
