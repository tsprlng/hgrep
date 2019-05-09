`hgrep`
=======

Hierarchical grep.

(Hierarchical only really means indentational.)

Not beautiful or efficient, but kind of oddly handy (for me).

There are a couple of things I use this for so far.

- I often keep notes in a text file full of hierarchical bullet points.

- I often configure "things" in big yaml (sadly) files which tend to be maps of maps of maps (this thing is therefore less good with lists).

Let's say you have a yaml file which is a bunch of config, and you want to decipher it in a specific way.

For example you know it's a list of things, many of which have a `"potato_type"` set. and you want to see all of the cases where the `potato_type` is set to something other than `green`.

```
$ hgrep -e potato_type -v green

potato_fields:
  field_a:
    potato_type: old
  field_b:
    potato_type: new
```

This weirdly seems to cover most of what I normally wish for, so it may never get cleverer than this.


Not what it could be
--------------------

There could be a ton of different options like...

- deal with .toml/.ini header/group things;

- print everything below the matched lines as well as / instead of everything above;

- whatever else

But there aren't.
