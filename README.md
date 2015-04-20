# hello-cron - basic demonstration of automatically running things with cron

# EXAMPLES

```
$ lib/shout
...
```

# INSTALL (run every 1 minute)

```
$ crontab -e
...

*/1 * * * * .../hello-cron/lib/shout

:wq
```

# UNINSTALL

```
$ crontab -e

dd

:wq
```

# REQUIREMENTS

* [mplayer](https://www.mplayerhq.hu/design7/news.html)

E.g., `brew install mplayer`
