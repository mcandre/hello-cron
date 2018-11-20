# hello-cron - basic demonstration of automatically running things with cron

# EXAMPLES

[gobbles.mp3](https://raw.githubusercontent.com/mcandre/hello-cron/master/gobbles.mp3)

```console
$ lib/shout
<Gobbles!>
```

# ABOUT

hello-cron provides a simple example of scheduling jobs with [cron / crond](https://en.wikipedia.org/wiki/Cron).

# LIST CRON JOBS

```console
$ crontab -l
```

# INSTALL

Use `crontab -e` to launch an interactive crontab editing session, each line representing an individual cron job. When you're ready, save and quit the editing session to effect your changes.

```console
$ crontab -e
...
:wq

$ crontab -l
* * * * * .../hello-cron/lib/shout
```

## As root user

```console
$ sudo crontab -u root -e
...
:wq
```

## Provision

```console
$ cp conf/shout.crontab /etc/cron.d/
```

# SYNTAX

See [conf](https://github.com/mcandre/hello-cron/tree/master/conf) examples.

# UNINSTALL

```console
$ crontab -e

dd

:wq
```

# REQUIREMENTS

* [cron](https://en.wikipedia.org/wiki/Cron)
* [mplayer](https://www.mplayerhq.hu/design7/news.html)

## Optional

* [shfmt](https://github.com/mvdan/sh) (e.g. `go get github.com/mvdan/sh/cmd/shfmt`)
* [bashate](https://github.com/openstack-dev/bashate)
* [shlint](https://rubygems.org/gems/shlint)
* [shellcheck](http://hackage.haskell.org/package/ShellCheck)
* [editorconfig-cli](https://github.com/amyboyd/editorconfig-cli) (e.g. `go get github.com/amyboyd/editorconfig-cli`)
* [stank](https://github.com/mcandre/stank) (e.g. `go get github.com/mcandre/stank/...`)
* [flcl](https://github.com/mcandre/flcl) (e.g. `go get github.com/mcandre/flcl/...`)
