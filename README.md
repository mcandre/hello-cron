# hello-cron - basic demonstration of automatically running things with cron

# EXAMPLES

[gobbles.mp3](https://raw.githubusercontent.com/mcandre/hello-cron/master/gobbles.mp3)

```
$ lib/shout
<Gobbles!>
```

# ABOUT

hello-cron provides a simple example of scheduling jobs with [cron / crond](https://en.wikipedia.org/wiki/Cron).

# LIST CRON JOBS

```
$ crontab -l
```

# INSTALL

Use `crontab -e` to launch an interactive crontab editing session, each line representing an individual cron job. When you're ready, save and quit the editing session to effect your changes.

```
$ crontab -e
...
:wq

$ crontab -l
@hourly /usr/local/Cellar/openssl-osx-ca/1.0.4/bin/openssl-osx-ca /usr/local/bin/brew
*/1 * * * * .../hello-cron/lib/shout
```

## As root user

```
$ sudo crontab -u root -e
...
:wq
```

## Provision

```
$ cp shout.crontab /etc/cron.d/
```

# SYNTAX

## Schedule once a minute

```
* * * * * .../hello-cron/lib/shout
```

# Schedule every 5 minutes

```
*/5 * * * * .../hello-cron/lib/shout
```

# Schedule every 50 minutes

```
*/50 * * * * .../hello-cron/lib/shout
```

# Schedule every 5 hours

```
* */5 * * * .../hello-cron/lib/shout
```

# Schedule every 5 days

```
* * */5 * * .../hello-cron/lib/shout
```

# Schedule every 5 weeks

```
* * */35 * * .../hello-cron/lib/shout
```

# Schedule every 5 months

```
* * * */5 * .../hello-cron/lib/shout
```

# Schedule every 5 years

```
* * * */60 * .../hello-cron/lib/shout
```

# Schedule every day at midnight

```
0 0 * * * .../hello-cron/lib/shout
```

# UNINSTALL

```
$ crontab -e

dd

:wq
```

# REQUIREMENTS

* [cron](https://en.wikipedia.org/wiki/Cron)
* [mplayer](https://www.mplayerhq.hu/design7/news.html)

E.g., `brew install mplayer`
