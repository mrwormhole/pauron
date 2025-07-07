# Pauron
Pauron is an automation bot for AUR repositories. You can think it of like watcher for github releases. The name emerges from Sauron but with "P" beginning. 

It patches PKGBUILD & .SRCINFO files when a new release is detected at upstream then pushes to AUR repository. This way, you can maintain more AUR repositories with less effort on updating new release versions.

> [!NOTE]  
> We only support GitHub upstream URLs for AUR packages.

### How to use 

You can fork this repo and tweak update-aur-packages.yaml after you have added `AUR_SSH_KEY` to GitHub secrets and adjust accordingly for your package name.

or

```sh
AUR_SSH_KEY="$(cat ~/.ssh/pauron)" pipx run pauron -p my-package-name
```

or

```sh
pipx install pauron
pipx ensurepath
AUR_SSH_KEY="$(cat ~/.ssh/pauron)" pauron -p my-package-name 
```
