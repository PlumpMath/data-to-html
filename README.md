# data-to-html

A Clojure library for converting data structures into html and opening them in a browser for inspection. It's very similar to clojure.inspector/inspect-tree but more readable to my eyes.

## Installation

```clojure
[data-to-html "0.1.2"]
```

## Usage

Import the project and its two functions

```clojure
(ns weather.core
  (require [data-to-html.core :refer [convert open-in-browser]]))
````

Define some data

```clojure
(def my-data {:temperature 27 :forecast #{:cloudy :rain :thunder}})
```

Run the data through *convert* to turn it into a html string. Use *open-in-browser* to save the string into a html page and make your OS open it in a browser.

```clojure
(-> my-data
    convert
    open-in-browser)
```

## Todo

* Generate docs from comments
* Helper function for doing it all
* Better css code
* Use tree walk instead
* Add foldable nodes to the tree
* Make sure lazy seqs and symbols work properly

## License

Copyright © 2013 Erik Svedäng

Distributed under the Eclipse Public License, the same as Clojure.
