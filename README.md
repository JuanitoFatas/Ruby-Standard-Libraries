Ruby Standard Libraries
=======================

Promote hidden gems in Ruby Stdlib.

Some stdlibs need to require before use it.

List of stdlibs that need to require
------------------------------------

TODO

Table of Content
----------------

* :gem: [Abbrev]()
* :gem: [English]()
* :gem: [Forwardable]()
* :gem: [Pathname]()

Abbrev
------

- Need to `require`? :o:
- [Official documentation](http://www.ruby-doc.org/stdlib-2.1.2/libdoc/abbrev/rdoc/Abbrev.html)

### Usage

`Abbrev#abbrev` will return **unique abbreviations** for a given set of strings:

signature: `abbrev(words, pattern = nil)`

### Example

```ruby
> require 'abbrev'
=> true

> puts Abbrev.abbrev(['ruby'])
=> {"ruby"=>"ruby", "rub"=>"ruby", "ru"=>"ruby", "r"=>"ruby"}
```

Optional parameter `pattern` can be a `Regexp` or `String`

`Regexp`: Will return result whose key contains given `pattern`:

```ruby
> Abbrev.abbrev(%w[python perl], /yt/)
=> {"python"=>"python", "pytho"=>"python", "pyth"=>"python", "pyt"=>"python", "py"=>"python", "perl"=>"perl", "per"=>"perl", "pe"=>"perl"}
```

`String`: Will return result whose key has *prefix* of `pattern`:

```ruby
> Abbrev.abbrev(%w[python perl], 'yt')
=> {}

> Abbrev.abbrev(%w[python perl], 'pyt')
=> {"python"=>"python", "pytho"=>"python", "pyth"=>"python", "pyt"=>"python"}
```

English
-------

- Need to `require`? :o:
- [Official documentation](http://www.ruby-doc.org/stdlib-2.1.2/libdoc/English/rdoc/English.html)

### Usage

Reference cryptic global variable with plain English.

Mappings

| Without English | With English                |
| --------------- | --------------------------- |
| `$!`            | `$ERROR_INFO`               |
| `$@`            | `$ERROR_POSITION`           |
| `$;`            | `$FS`                       |
| `$;`            | `$FIELD_SEPARATOR`          |
| `$,`            | `$OFS`                      |
| `$,`            | `$OUTPUT_FIELD_SEPARATOR`   |
| `$/`            | `$RS`                       |
| `$/`            | `$INPUT_RECORD_SEPARATOR`   |
| `$\`            | `$ORS`                      |
| `$\`            | `$OUTPUT_RECORD_SEPARATOR`  |
| `$.`            | `$INPUT_LINE_NUMBER`        |
| `$.`            | `$NR`                       |
| `$_`            | `$LAST_READ_LINE`           |
| `$>`            | `$DEFAULT_OUTPUT`           |
| `$<`            | `$DEFAULT_INPUT`            |
| `$$`            | `$PID`                      |
| `$$`            | `$PROCESS_ID`               |
| `$?`            | `$CHILD_STATUS`             |
| `$~`            | `$LAST_MATCH_INFO`          |
| `$=`            | `$IGNORECASE`               |
| `$*`            | `$ARGV`                     |
| `$&`            | `$MATCH`                    |
| `$``            | `$PREMATCH`                 |
| `$‘`            | `$POSTMATCH`                |
| `$+`            | `$LAST_PAREN_MATCH`         |

### Example

```ruby
require "English"

$OUTPUT_FIELD_SEPARATOR = ' -- '
"waterbuffalo" =~ /buff/
print $LOADED_FEATURES, $POSTMATCH, $PID, "\n"
```

Contributing
------------

TODO

How to Contribute?
------------------

TODO

Read [CONTRIBUTING](/CONTRIBUTING.md)

License
-------

![CC-BY-SA](CC-BY-SA.png)

[Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

Author
------

:yellow_heart: :blue_heart: :purple_heart: :heart: :green_heart: :heartbeat: :heartpulse: :two_hearts: :revolving_hearts: :cupid: :sparkling_heart:

Written with love by @juanitofatas :sunglasses:.
