# naucse_render

Helper for converting course material in YAML/Markdown/Jupyter to
naucse.python.cz JSON API.

## Version 0

naucse_render 0.x should successfully render courses hosted on naucse.python.cz
prior to 2019.

The format of the source files grew organically, so there is no attempt here
to document it.


# Entrypoints

There are two public entrypoints: one for getting general course information;
the other for a subset of lessons.

(This separation means the content doesn't need to be rendered to get course
info.)

`naucse_render.get_course(course_slug, *, path='.', version=None)`

`naucse_render.get_lessons(lesson_slugs, vars=None, path='.')`

The `path` specifies the local filesystem path to the root of the repository
(i.e. parent directory of `courses`, `runs` and `lessons`).


# Installation & Usage

This is meant as a dependency in other repos. Use instructions there.


## Tests

To tests, install `pipenv`, and install dependencies:

```console
$ pipenv install --dev
```

then run the tests:

```console
$ pipenv run test
```


# License

The code is licensed under the terms of the MIT license, see [LICENSE.MIT] file
for full text. By contributing code to this repository, you agree to have it
licensed under the same license.

[LICENSE.MIT]: https://github.com/pyvec/naucse.python.cz/blob/master/LICENSE.MIT