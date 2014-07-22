# midje-readme

A Leiningen plugin to pull tests from your README.md into midje automatically. This will make it easy to make sure your readme doesn't contain any errors.

## Usage

Put `[midje-readme "1.0.0"]` into the `:plugins` vector of your project.clj.

By default midje-readme will put "(:require [your-project.core :refer :all])" into the test file. You can override this by putting ":midje-readme {:require "[your-project.something-else :refer [whatever]]"}" into your project.clj.


When you run a leiningen command the plugin will create a file "test/readme.clj" that contains the code in your readme. Line numbers will be the same as in your readme so debugging should be pretty easy.

You might want to add test/readme.clj to your .gitignore too.

## Restrictions

Changes in README.md will not be picked up by "lein midje :autotest"
