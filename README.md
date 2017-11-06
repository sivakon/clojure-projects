# Clojure stuff

### the links to learn Clojure is below

- After installing `lein`, we can update `~/.lein/profiles.clj` to include some packages while starting. Please add the following code 

```clojure
{:user
  {:dependencies [[alembic "0.3.2"]]
   :plugins [[com.palletops/lein-shorthand "0.4.0"]]
   :shorthand {. [alembic.still/distill alembic.still/lein]}}}
```

- In gorilla repl, we can use 
```clojure
(require 'alembic.still)
(alembic.still/distill '[[org.clojure/clojure "1.6.0"]
               [incanter "1.5.7"]])
```

- We can also add all the required libraries in `project.clj` file.
- Get gorilla repl integration with Incanter [Link](https://github.com/JonyEpsilon/incanter-gorilla)

- Once the worksheet is hosted at github. We can use [this link](http://viewer.gorilla-repl.org/view.html?source=github&user=sivakon&repo=clojure-projects&path=my-stuff/graph-examples.clj) to get the complete worksheet online


Clojure tutorial here.
[Link here](https://kimh.github.io/clojure-by-example/#scope)


## Project definition for data-analysis
```clojure
;; project.clj file for the current project
(defproject data-analysis "0.1.0-SNAPSHOT"
  :description "FIXME: write description"
  :url "http://example.com/FIXME"
  :license {:name "Eclipse Public License"
            :url "http://www.eclipse.org/legal/epl-v10.html"}
  :dependencies [[org.clojure/clojure "1.8.0"]
                 [incanter "1.5.7"]])
```


## Setup .lein folder in its installation folder 
- Copy the following code in the `profiles.cjl` file.
```clojure
{:repl {:plugins [[cider/cider-nrepl "0.16.0-SNAPSHOT"]]}}

{:user
  {:dependencies [[alembic "0.3.2"]
                  [incanter "1.5.7"]]
   :plugins [[com.palletops/lein-shorthand "0.4.0"]]
   :shorthand {. [alembic.still/distill alembic.still/lein]}}}
```

## Start the repl in the folder as usual (it is better in the project folder)
- With emacs, first install cider.
- `cider-connect` to the existing repl. Please provide localhost and port number after you start the repl in console.
- Cider will now be connected to the existing repl.
- Start the repl in the console with `lein repl`
