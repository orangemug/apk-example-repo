# apk-example-repo
A demo [apk-packager](https://github.com/orangemug/apk-packager) repository

[![stability-wip](https://img.shields.io/badge/stability-work_in_progress-lightgrey.svg)][stability]
[![Build Status](https://circleci.com/gh/orangemug/apk-example-repo.png?style=shield)][circleci]
[![Dependency Status](https://david-dm.org/orangemug/apk-example-repo.svg)][dm-prod]
[![Dev Dependency Status](https://david-dm.org/orangemug/apk-example-repo/dev-status.svg)][dm-dev]

[stability]:   https://github.com/orangemug/stability-badges#work-in-progress
[circleci]:    https://circleci.com/gh/orangemug/apk-example-repo
[dm-prod]:     https://david-dm.org/orangemug/apk-example-repo
[dm-dev]:      https://david-dm.org/orangemug/apk-example-repo#info=devDependencies

The repository uses the [apk-packager](https://github.com/orangemug/apk-packager) to build packages into a github release (see <https://github.com/orangemug/apk-example-repo/releases/tag/master/x86_64>)


## Requirements
You'll need alpine linux installed in order to use this repository. If you are not running alpine linux you can boot up an instance with docker now (assumes you have docker instaled)

```sh
$ docker run -i -t alpine /bin/sh
```


## Usage
Setup the repository

```sh
$ apk add update \
  --allow-untrusted \
  --repository 'https://github.com/orangemug/apk-example-repo/releases/download/master'
```

Install its only package [hello-world](https://github.com/orangemug/hello-world)

```sh
$ apk add hello-world
```

Now run `hello-world` to prove it installed

```sh
$ hello-world
Hello World
```


## License
[MIT](LICENSE)