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

Simply push to Heroku or a Dokku

### Dokku configuration

It's a good idea to keep your secret access tokens outside of the repo. If you use Dokku you can easily add tokens as ENV variables and reference them from the tutter.yaml file.

**Example**

```
$ dokku config:set tutter TESTING_TOKEN=your_token_here
```

```yaml
projects:
  - name: 'jpettersson/testing'
    access_token_env_var: 'TESTING_TOKEN'
    github_site: 'https://github.com'
    github_api_endpoint: 'https://api.github.com'

    action: 'thanks'
```
