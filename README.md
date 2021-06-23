Description
===========

A script to use with [fzf][fzf] for previews.
Can preview arbitrary files, including videos/PDF.
Uses [kitty][kitty]'s [icat kitten][icat] to show images, but can be modified
to use other methods such as w3mimgdisplay.
Piggybacks on [ranger][ranger]'s cache directory (if present) to avoid
duplicating preview files.


Usage
=====

Download and place the script in your `$PATH`, for example:

    cd ~/.local/bin/
    wget 'https://github.com/GermainZ/fzf-preview/raw/master/fzf-preview'
    chmod +x fzf-preview

Then invoke it from fzf, for example:

    fzf --preview 'fzf-preview {}'


Screencast
==========

![Screencast](screencast.gif?raw=true "Screencast")

Licenses for media used in the screencast:
- ["Quiet morning - HDR, no example for D300 noise"](https://www.flickr.com/photos/58837045@N00/2105626736) by [christianmeichtry](https://www.flickr.com/photos/58837045@N00) is licensed under [CC BY-NC-SA 2.0](https://creativecommons.org/licenses/by-nc-sa/2.0/).
- ["A fine example of writing"](https://www.flickr.com/photos/77005536@N00/456033137) by [churl](https://www.flickr.com/photos/77005536@N00) is licensed with [CC BY-NC-ND 2.0](https://creativecommons.org/licenses/by-nc-nd/2.0/).
- ["Made with Creative Commons"](https://creativecommons.org/use-remix/made-with-cc/) by [Paul Stacey and Sarah Hinchliff Pearson of Creative Commons](https://creativecommons.org/) is licensed with [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
- ["Big Buck Bunny"](https://peach.blender.org/) (c) copyright 2008, Blender Foundation / [www.bigbuckbunny.org](https://bigbuckbunny.org/) is licensed with [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/).
- ["Sintel"](https://durian.blender.org/) © copyright Blender Foundation | [durian.blender.org](https://durian.blender.org/) is licensed with [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/).


Dependencies
============

- [fzf][fzf]
- Image previews: [kitty][kitty] is used, but you can edit
  `clear_image_preview()` and `preview_image()` to use another tool.

For previews:
- Videos: [ffmpegthumbnailer](https://github.com/dirkvdb/ffmpegthumbnailer)
- PDFs: pdftoppm, part of [Poppler](https://poppler.freedesktop.org/)
- Audio files: [mediainfo](https://mediaarea.net/en/MediaInfo)
- Everything else: [bat](https://github.com/sharkdp/bat)


[fzf]: https://github.com/junegunn/fzf
[kitty]: https://sw.kovidgoyal.net/kitty/
[icat]: https://sw.kovidgoyal.net/kitty/kittens/icat.html
[ranger]: https://github.com/ranger/ranger/
