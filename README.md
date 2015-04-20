# hello-cron - basic demonstration of automatically running things with cron

# EXAMPLES

[gobbles.mp3](https://raw.githubusercontent.com/mcandre/hello-cron/master/gobbles.mp3)

```
$ lib/shout
<Gobbles!>
```

# ABOUT

hello-cron provides a simple example of scheduling jobs with [cron / crond](https://en.wikipedia.org/wiki/Cron).

# INSTALL

```
$ crontab -e
...
:wq
```

## Schedule once a minute

```
*/1 * * * * .../hello-cron/lib/shout
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
