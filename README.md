# PokeMMO flatpak

## Description

This is a flatpak for [PokeMMO][PokeMMO]. Currently no permission from
upstream to publish this to flathub yet (see [this forum
thread][thread]), sadly.

In case we ever get permission (or enough time passes that we'd like
to publish without permission, this isn't redistribution after all),
we should first fix:

- [x] File verification fails on start
  - Fixed in 9900147c64f2b1d684e49d63e243465ca102f1f3
- [x] Not using portals to supply ROMs
  - This was fixed by simply removing the `--persist` directory, I
    suppose not having these allows flatpak to do nice things.
- [x] Translations are missing
  - Only broken in a commit I never published
- [ ] No license to use icons from upstream
- [ ] The StartupWMClass may be wrong
- [ ] x-checker-data is untested
- [ ] No screenshots or other niceties

## Building and installing

In the mean time, if you do want to use this, simply clone this
repository, run flatpak-builder to build locally, and enjoy the
flatpak:

```bash
git clone -b new-pr https://github.com/tlater/flathub
cd flathub && flatpak-builder --user --install build eu.pokemmo.PokeMMO.yml
```

[PokeMMO]: https://pokemmo.eu
[thread]: https://forums.pokemmo.eu/index.php?/topic/95408-publish-the-software-as-snap/#comment-1749867
