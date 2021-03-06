Ruby Standard Libraries
=======================

Promote hidden gems in Ruby Stdlib.

Target version: Ruby 2.1.2.

[Official Documentation links](http://www.ruby-doc.org/stdlib-2.1.2/).

[Where does Ruby Stadard Libraries live?][rubystdlib]

[rubystdlib]: https://github.com/ruby/ruby/tree/trunk/lib

Table of Content
----------------

List alphabetically:

* :gem: [Abbrev](#abbrev)
* :gem: [English](#english)
* :gem: [Forwardable](#forwardable)
* :gem: [OpenStruct](#openstruct)
* :gem: [Pathname](#pathname)
* :gem: [Shellwords](#shellwords)
* :gem: [Singleton](#singleton)
* :gem: [YAML::Store](#yamlstore)

Abbrev
------

- [Official documentation](http://www.ruby-doc.org/stdlib-2.1.2/libdoc/abbrev/rdoc/Abbrev.html) :arrow_upper_right:

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

Optional parameter `pattern` can be a `Regexp` or `String`.

`Regexp`: Will return result whose key contains given `pattern`:

```ruby
> Abbrev.abbrev(%w[python perl], /yt/)
=> {"python"=>"python", "pytho"=>"python", "pyth"=>"python", "pyt"=>"python"}
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

- [Official documentation](http://www.ruby-doc.org/stdlib-2.1.2/libdoc/English/rdoc/English.html) :arrow_upper_right:

### Usage

Reference cryptic global variable with plain English.

Mappings

| Without English | With English                | Without English | With English                |
| --------------- | --------------------------- | --------------- | --------------------------- |
| `$!`            | `$ERROR_INFO`               | `$>`            | `$DEFAULT_OUTPUT`           |
| `$@`            | `$ERROR_POSITION`           | `$<`            | `$DEFAULT_INPUT`            |
| `$;`            | `$FS`                       | `$$`            | `$PID`                      |
| `$;`            | `$FIELD_SEPARATOR`          | `$$`            | `$PROCESS_ID`               |
| `$,`            | `$OFS`                      | `$?`            | `$CHILD_STATUS`             |
| `$,`            | `$OUTPUT_FIELD_SEPARATOR`   | `$~`            | `$LAST_MATCH_INFO`          |
| `$/`            | `$RS`                       | `$=`            | `$IGNORECASE`               |
| `$/`            | `$INPUT_RECORD_SEPARATOR`   | `$*`            | `$ARGV`                     |
| `$\`            | `$ORS`                      | `$&`            | `$MATCH`                    |
| `$\`            | `$OUTPUT_RECORD_SEPARATOR`  | `$``            | `$PREMATCH`                 |
| `$.`            | `$INPUT_LINE_NUMBER`        | `$‘`            | `$POSTMATCH`                |
| `$.`            | `$NR`                       | `$+`            | `$LAST_PAREN_MATCH`         |
| `$_`            | `$LAST_READ_LINE`           |                 |                             |

### Example

```ruby
require 'English'

$OUTPUT_FIELD_SEPARATOR = ' -- '
'waterbuffalo' =~ /buff/
print $LOADED_FEATURES, $POSTMATCH, $PID, "\n"
```

Forwardable
-----------

- [Official documentation]()

### Usage

### Example

OpenStruct
-----------

- [Official documentation]()

### Usage

### Example

Pathname
-----------

- [Official documentation]()

### Usage

### Example

Shellwords
-----------

- [Official documentation]()

### Usage

### Example

Singleton
-----------

- [Official documentation]()

### Usage

### Example

YAML::Store
-----------

- [Official documentation](http://ruby-doc.org/stdlib-2.1.2/libdoc/yaml/rdoc/YAML/Store.html)

### Usage

### Example


Questions? Suggestions?
-----------------------

[Tell me!][issues]

[issues]: https://github.com/JuanitoFatas/Ruby-Standard-Libraries/issues/new

How to Contribute?
------------------

Read [CONTRIBUTING](/CONTRIBUTING.md).

License
-------

![CC-BY-SA](CC-BY-SA.png)

[Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

Author
------

:yellow_heart: :blue_heart: :purple_heart: :heart: :green_heart: :heartbeat: :heartpulse: :two_hearts: :revolving_hearts: :cupid: :sparkling_heart: :two_hearts: :yellow_heart: :purple_heart: :sparkling_heart: :green_heart: :heartpulse: :heart: :cupid: :heartbeat: :revolving_hearts: :blue_heart:

*Written with love by @juanitofatas :sunglasses:.*
