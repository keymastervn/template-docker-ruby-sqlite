### Attention

[Original](https://docs.docker.com/compose/rails/)

> I guess I may run different web framework such as sinatra, so I will change what should be changed. However, most of the cases involve custom configs / data layer (model) / sometimes authentication (login devise) / API, who did better than rails?

Step 1: initialize rails

```bash
$ docker-compose run --no-deps web rails new . --force

# or API only: --api
```

Step 2: build the container

```bash
$ docker-compose build
```

Step 3: run

```bash
$ docker-compose up
```

You may miss something!

#### Additional

Prerequisite

```bash
$ docker-compose run web rails db:create

# or rails 6, running create, migrate, seed at once: rails db:prepare
```

Run test

```bash
$ docker-compose run web rails test

# or rspec: bundle exec rspec --profile 10 --format progress spec/**/*_test.rb
```


### Resources

Useful commands

- [Rails generator cheatsheet](https://gist.github.com/cdesch/2f8de645cad1d83aa251c0a20b0f7097)
- [curl -X method -d 'name=a&age=10'](https://linux4one.com/15-curl-command-examples-in-linux)
