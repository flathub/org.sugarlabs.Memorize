# Memorize Activity Flatpak

Memorize is about finding matching pairs. A pair can be images, sounds and text and this could be extended to animations or movie snippets as well. Which pairs match is up to the creator of the game. Memorize is more than a predefined game you can play, it allows you to create new games yourself as well.

To know more refer: https://github.com/sugarlabs/memorize-activity

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.Memorize.git
cd org.sugarlabs.Memorize
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.Memorize.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Memorize
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Memorize.json
```