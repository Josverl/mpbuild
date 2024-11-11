# mpbuild

## Usage

```bash
> mpbuild build BOARD [VARIANT] -- [EXTRA_ARGS]
```

```bash
> mpbuild clean BOARD [VARIANT]
```

```bash
> mpbuild list [--port PORT]
```

- Should it list boards and variants? (yes, probably. Alternatively, '-a'.)

## Example

To build with additional parameters such as `USER_C_MODULES`:

```bash
> mpbuild build ESP32_GENERIC_S3 -- USER_C_MODULES=/home/user/micropython/ulab/code/micropython.cmake all
```

## Development

- rye for managing the project
- Use ruff for formatting
- pre-commit
  - ruff formatting and linting

## todo

- Check we're at the root of a MicroPython repo
- Tab completion for board names and ports
- May want a way to override the container used for building?
- Add interative modes (textual?) to select boards/variants
- Fix version - only use the version number from pyproject.toml
  - And query it with importlib.metadata.version
- Check docker is in the path
- IDF version should be configurable
- Add unix and webassembly 'special' builds (no boards, build by port name)
