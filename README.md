# stem skeleton v0.1

Cell with predefined dna to be developed as 'backend', 'frontend' or both

## use

1. `$ mkdir ./mypetproject`
1. `$ cd ./mypetproject`
1. `$ npm install outbounder/organic-stem-skeleton angelscripts-stack-use`
1. `$ angel stack use core`
1. `$ mv ./gitignore ./.gitignore` [needed because of this](https://github.com/npm/npm/issues/11061)
1. add any stack upgrades (run `$ angel stack list` for available options)
1. `$ angel stack configure`
1. `git init . && git add --all && git commit`

___notice 1)___
`angel` is organic command line assistant.
Either install it via `npm install organic-angel -g` or install it locally and always run via `node ./node_modules/.bin/angel`.

___notice 2)___
Running `$ angel help` will print all available commands to your disposal.

### stack upgrades

#### server

##### mocha-chai

    $ angel stack use mocha-chai

##### emails support

    $ angel stack use emails-support

##### mongoose models

    $ angel stack use mongoose

##### mongodb stored cookie based sessions

    $ angel stack use mongo-sessions

##### server rendered pages

###### ejs templates

    $ angel stack use ejs-pages

###### jade templates

    $ angel stack use jade-pages

#### devtools

Refer to [devtools](https://github.com/outbounder/organic-stem-devtools) or `$ angel stack list`

    $ npm install organic-stem-devtools
    $ angel stack use devtools
    ... any other devtools stack upgrades (see them via $ angel stack list)

#### frontend SPAs

###### backbone + jade templates

    $ angel stack use jade-backbone

###### angular1

    $ angel stack use angular1

###### react + flux

    $ angel stack use react-flux

###### organic-oval + plasma + form-tag + bind-tag + router + other organic goodies ;)

    $ angel stack use organic-oval-fu


## how to run tests

1. define `mock-stemskeleton.json` into the repo's root folder

  ```
  $ cd organic-stem-skeleton
  $ echo '"/full/path/to/stem-seed"' > mock-stemskeleton.json
  ```

2. prepare mocked stem skeleton seed folder

  ```
  $ cd /full/path/to/stem-seed
  $ npm install angelscripts-stack-use
  $ npm link /full/path/to/organic-stem-skeleton
  $ npm install organic-stem-devtools
  ```
