# glistix_example

[![Package Version](https://img.shields.io/hexpm/v/glistix_example)](https://hex.pm/packages/glistix_example)
[![Hex Docs](https://img.shields.io/badge/hex-docs-ffaff3)](https://hexdocs.pm/glistix_example/)

```sh
glistix add glistix_example
```
```gleam
import glistix_example

pub fn main() {
  // TODO: An example of the project in use
}
```

**Note:** This is a Glistix project, and as such may require the
[Glistix compiler](https://github.com/glistix/glistix) to be used.

Further documentation can be found at <https://hexdocs.pm/glistix_example>.

## Importing from Nix

To import this project from Nix, first fetch its source (through a Flake input,
using `builtins.fetchGit`, cloning to a local path, or some other way), import
the Flake or the `default.nix` file, and run `lib.loadGlistixPackage { }`.
For example:

```nix
let
  # Assuming the project was cloned to './path/to/project'
  glistix_example = import ./path/to/project;
  # Use 'loadGlistixPackage { module = "module/name"; }' to pick a module
  package = glistix_example.lib.loadGlistixPackage { };
  result = package.main { };
in result
```

## Development

```sh
nix develop   # Optional: Spawn a shell with glistix
glistix run   # Run the project
glistix test  # Run the tests
```
