<div align="center">

![Password Pusher Front Page](https://disznc.s3.amazonaws.com/Screen-Shot-2021-07-04-at-9.04.09-PM.png)

__Simple & Secure Password Sharing with Auto-Expiration of Shared Items__
    
[![](https://badgen.net/twitter/follow/pwpush)](https://twitter.com/pwpush)
![](https://badgen.net/github/stars/pglombardo/PasswordPusher)
![](https://badgen.net/uptime-robot/month/m789048867-17b5770ccd78208645662f1f)
[![](https://badgen.net/docker/pulls/pglombardo/pwpush-ephemeral)](https://hub.docker.com/repositories)

[![Github CI](https://github.com/pglombardo/PasswordPusher/actions/workflows/ruby.yml/badge.svg)](https://github.com/pglombardo/PasswordPusher/actions/workflows/ruby.yml)
[![](https://badgen.net/circleci/github/pglombardo/PasswordPusher)](https://circleci.com/gh/pglombardo/PasswordPusher/tree/master)
[![Dependencies Status](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg)](https://github.com/pglombardo/pwpush-cli/pulls?utf8=%E2%9C%93&q=is%3Apr%20author%3Aapp%2Fdependabot)
[![Semantic Versions](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--versions-e10079.svg)](https://github.com/pglombardo/pwpush-cli/releases)
[![License](https://img.shields.io/github/license/pglombardo/PasswordPusher)](https://github.com/pglombardo/pwpush/blob/master/LICENSE)

</div>

------

Password Pusher is an opensource application to communicate passwords over the web. Links to passwords expire after a certain number of views and/or time has passed.

Hosted at [pwpush.com](https://pwpush.com) but you can also easily run your own private instance with just a few steps.

* __Easy-to-install:__ Host your own via Docker, a cloud service or just use [pwpush.com](https://pwpush.com)
* __Opensource:__ No blackbox code.  Only trusted, tested and reviewed opensource code.
* __Audit logging:__ Track and control what you've shared and see who has viewed it.
* __Encrypted storage:__ All sensitive data is stored encrypted and is deleted once expired.
* __Host your own:__ Database backed or ephemeral, easily run your own instance isolated from the world.
* __JSON API:__ Raw JSON API available for 3rd party tools or command line via `curl` or `wget`.
* __Command line interface:__ Automate your password distribution with CLI tools or custom scripts.
* __Internationalized:__ 10 language translations are bundled in.  Easily selectable via UI or URL
* __Unbranded delivery page:__ No logos, superfluous text or unrelated links to confuse end users.
* __Customizable:__ Change text and default options via environment variables.
* __Light & dark themes:__  Via CSS @media integration, the site theme follows your local preferences
* __10 Years Old:__ Password Pusher has securely delivered millions and millions of passwords in it's 10 year history.
* __Honest Software:__  Opensource written and maintained by [me](https://github.com/pglombardo) with the help of some great contributors.  No organizations, corporations or evil agendas.

Follow Password Pusher [on Twitter](https://twitter.com/pwpush), [Gettr](https://gettr.com/user/pwpush) or [on Facebook](https://www.facebook.com/pwpush) for the latest news, updates and changes.

-----

# How to Use

You can access Password Pusher at [pwpush.com](https://pwpush.com) or alternatively use one of the tools below.

To run your own instance, see [Run Your Own Instance](#-run-your-own-instance) in the next section.

## Command Line Utilities

* [pgarm/pwposh](https://github.com/pgarm/pwposh): a PowerShell module available in the [PowerShell Gallery](https://www.powershellgallery.com/packages/PwPoSh/)

*  [kprocyszyn/Get-PasswordLink.ps1](https://github.com/kprocyszyn/tools/blob/master/Get-PasswordLink/Get-PasswordLink.ps1): a PowerShell based CLI

*  [lnfnunes/pwpush-cli](https://github.com/lnfnunes/pwpush-cli): a Node.js based CLI 

* [abkierstein/pwpush](https://github.com/abkierstein/pwpush): a Python based CLI

## Android Apps

*  [Pushie](https://play.google.com/store/apps/details?id=com.chesire.pushie) by [chesire](https://github.com/chesire)

## Application Integrations

* [Slack: How to Add a Custom Slash Command](https://github.com/pglombardo/PasswordPusher/wiki/PasswordPusher-&-Slack:-Custom-Slash-Command)

* [Alfred Workflow](http://www.packal.org/workflow/passwordpusher) for Mac users

## API

* [JSON API](https://github.com/pglombardo/PasswordPusher/wiki/Password-API)



# 💾 Run Your Own Instance

_Note: Password Pusher can be largely configured by environment variables so after you pick your deployment method below, make sure to read [the configuration page](Configuration.md).  Take particular attention in setting your own custom encryption key which isn't required but provides the best security for your instance._

## On Docker

Docker images of Password Pusher are available on [Docker hub](https://hub.docker.com/u/pglombardo).

**➜ ephemeral**

    docker run -d -p "5100:5100" pglombardo/pwpush-ephemeral:release

[Learn more](https://github.com/pglombardo/PasswordPusher/tree/master/containers/docker#pwpush-ephemeral)

**➜ using an External Postgres Database**

    docker run -d -p "5100:5100" pglombardo/pwpush-postgres:release

[Learn more](https://github.com/pglombardo/PasswordPusher/tree/master/containers/docker#pwpush-postgres-external-database)

_Note: The `latest` Docker container tag builds nightly off of the latest code changes and can occasionally be unstable.  Always use the ['release' or version'd tags](https://hub.docker.com/repository/docker/pglombardo/pwpush-ephemeral/tags?page=1&ordering=last_updated) if you prefer more stability in releases._

## With Docker Compose

Included in this repository is `containers/docker/pwpush-postgres/docker-compose.yaml` which can be used by simply running:

    docker-compose up -d
    docker-compose down

[Learn more](https://github.com/pglombardo/PasswordPusher/tree/master/containers/docker#pwpush-postgres)

## On Kubernetes

Instructions and explanation of a Kubernetes setup [can be found
here](https://github.com/pglombardo/PasswordPusher/tree/master/containers/kubernetes).

## On Microsoft Azure

_There used to be a 3rd party blog post with instructions but it's been deleted.  If anyone has instructions they would like to contribute, it would be greatly appreciated._

See issue #277

## On OpenShift

See our [OpenShift documentation](https://github.com/pglombardo/PasswordPusher/tree/master/containers/docker#pwpush-openshift).

## On Heroku

One click deploy to [Heroku Cloud](https://www.heroku.com) without having to set up servers.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/pglombardo/PasswordPusher)

_This option will deploy a production Password Pusher instance backed by a postgres database to Heroku.  As is monthly cost: $0._

## From Source

Make sure you have git and Ruby installed and then:

```sh
git clone git@github.com:pglombardo/PasswordPusher.git
cd PasswordPusher
gem install bundler
bundle install --without development production test --deployment
bundle exec rake assets:precompile
RAILS_ENV=private bundle exec rake db:setup
foreman start internalweb
```

Then view the site @ [http://localhost:5100/](http://localhost:5100/).

# 📼 Credits

## Translators

Thanks to our great translators.  We'll fill this area out more as we add more languages.

* Łukasz ([Github](https://github.com/drpt)) for Polish
* Thomas @ confluencepoint ([Github](https://github.com/confluencepoint/) | [Twitter](https://twitter.com/confluencepoint)) for German

Also thanks to [translation.io](https://translation.io) for their great service in managing translations.  It's also generously free for opensource projects.

## Containers

Thanks to:

* [@fiskhest](https://github.com/fiskhest) the [Kubernetes installation instructions and manifests](https://github.com/pglombardo/PasswordPusher/tree/master/containers/kubernetes).

* [@sfarosu](https://github.com/sfarosu) for [contributing](https://github.com/pglombardo/PasswordPusher/pull/82) the Docker, Kubernetes & OpenShift container support.

## Other

Thanks to:

* [@iandunn](https://github.com/iandunn) for better password form security.

* [Kasper 'kapöw' Grubbe](https://github.com/kaspergrubbe) for the [JSON POST fix](https://github.com/pglombardo/PasswordPusher/pull/3).

* [JarvisAndPi](http://www.reddit.com/user/JarvisAndPi) for the favicon design

...and many more.  See the [Contributors page](https://github.com/pglombardo/PasswordPusher/graphs/contributors) for more details.
