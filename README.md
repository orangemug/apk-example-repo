# apk-example-repo
A demo [apk-packager](https://github.com/orangemug/apk-packager) repository

[![stability-wip](https://img.shields.io/badge/stability-work_in_progress-lightgrey.svg)][stability]
[![Build Status](https://circleci.com/gh/orangemug/apk-example-repo.png?style=shield)][circleci]

[stability]:   https://github.com/orangemug/stability-badges#work-in-progress
[circleci]:    https://circleci.com/gh/orangemug/apk-example-repo

The repository uses the [apk-packager](https://github.com/orangemug/apk-packager) to build packages into a github release (see <https://github.com/orangemug/apk-example-repo/releases/tag/master/x86_64>)


## Requirements
You'll need alpine linux installed in order to use this repository. If you are not running alpine linux you can boot up an instance with docker now (assumes you have docker instaled)

```sh
$ docker run -i -t alpine /bin/sh
```


## Usage
Install its only package [hello-world](https://github.com/orangemug/hello-world)

```sh
$ apk add \
  --allow-untrusted \
  --repository 'https://github.com/orangemug/apk-example-repo/releases/download/master' \
  hello-world
```

Now run `hello-world` to prove it installed

```sh
$ hello-world
Hello World
```


## License
[MIT](LICENSE)
