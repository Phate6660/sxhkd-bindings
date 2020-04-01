# sxhkd-bindings
A low quality shell script to parse and display keybindings + descriptions.

# Requirements
- Grep
- Sed
- Rofi
- sxhkdrc setup in the proper format (more info below)

# sxhkdrc format
In order to parse properly, you need to place some stuff into your rc file.<br>
You need to place a one line comment directly above a keybinding with this format: `description: DESCRIPTION`.

For example:
```
# description: transparent uxterm
alt + Return
    uxterm & sleep 0.25 && transset -a 0.8
```

Which will output:<br>
![example](screenshots/example.png)

And here is what a more full example would look like:<br>
![full example](screenshots/full_example.png)

Note: Your rofi will look different due to using a different theme.<br>
If you like the one I'm using, you may find it [here](https://github.com/Phate6660/dotfiles/blob/master/.cache/wal/colors-rofi-dark.rasi) in my [dotfiles repo](https://github.com/Phate6660/dotfiles).

# Installation
1. `curl -sSL https://raw.githubusercontent.com/Phate6660/sxhkd-bindings/master/sxhkd-bindings -o sxkhkd-bindings`
2. Inspect the script. Don't run scripts from the internet without checking them.
3. `chmod +x sxhkd-keybindings`
4. Move the script to anywhere in your `$PATH` and run the command (e.g. `sxhkd-bindings`), or just run it as is (e.g. `./sxhkd-bindings`).
