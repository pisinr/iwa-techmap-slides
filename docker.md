# Docker

---

## A recipe for service.

```Dockerfile
FROM ubuntu:16.04

RUN apt-get update && apt-get install -y \
  git imagemagick ruby
RUN git clone ssh://service.repo/code.git
RUN gem install bundler

CMD RAILS_ENV=production bundle exec rails s
```

* make sure the build script is reproducible.

^^^

### A tiny mini VM

* Only single service


^^^

### docker-compose

* Run multiple services together

```yml
services:
    app:
        image: bestapp:1.5.2
    db:
        image: postgresql:9.1
    redis:
        image: redis:2.3
```