# rebar_subdirs_output

## Overview

STATUS: IN PROGRESS (not working as intended yet, just started)

The purpose of this Rebar plugin/extension is to output the full path
upon a compilation error even when the file is located in one of the
configured `subdirs` when invoked from a multi-subdir project.

For example, say you have a project called `abc`. It has a
`rebar.config` file that looks something like this:

```erlang
{deps_dir, ["deps"]}.
{deps, [
  % your dependencies here
]}.
{sub_dirs, ["apps/abc_web", "apps/abc_voip", "apps/abc_api"]}.```

You have three subdirectories that are part of this parent project:
* `apps/abc_web`
* `apps/abc_voip`
* `apps/abc_api`

Each of these subdirectories contain their own `rebar.config` file with
their own specific dependencies and options defined.

Without this plugin/extension to Rebar the output of upon on a
compilation error (in say abc_voip) will look something like this:

```
==> abc_web (compile)
==> abc_voip (compile)
src/abc_voip_util.erl:9: Erlang error message goes here.
```

With this plugin/exension to Rebar this output will look like this:

```
==> abc_web (compile)
==> abc_voip (compile)
apps/abc_voip/src/abc_voip_util.erl:9: Erlang error message goes here.
```

## Installation

To install this Rebar plugin/exension you just need to add it as a
dependency to your top level project and then

## Author(s)

* Susan Potter <me@susanpotter.net>

## License

This is licensed under a 3-clause BSD license. See LICENSE file for details.

## Copyright

Copyright (c) 2011 Susan Potter <me@susanpotter.net>.  All rights reserved.
