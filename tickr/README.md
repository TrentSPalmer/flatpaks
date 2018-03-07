# How To Use
flatpak for tickr rss feed reader, a gtk2 application written in c.

As far as this experimental packaging
attempt goes, it can open links in a web browser by calling `xdg-open`, so presumably some kind
of desktop environment is required, but seems to have all the dependancies it needs from the
flathub gnome platform runtime.

[http://www.open-tickr.net](http://www.open-tickr.net)

## build tickr flatpak into local repo directory

```bash
flatpak-builder --repo=/home/$USER/repo --force-clean /home/$USER/tickr com.tickr.Tickr.json
```

## add local repo directory as a repo

```bash
flatpak --user remote-add --no-gpg-verify local-repo repo
```

## install tickr flatpak from the local repo

```bash
flatpak --user install local-repo com.tickr.Tickr
```

If you need to change the repository settings, those will be in
`~/.local/share/flatpak/repo/config`

## issues

* no ssl/tls encrypted rss feeds, http only
* shortcuts don't work unless you enable window decoration, but that gives your tickr a big ugly window decoration
