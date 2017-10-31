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
