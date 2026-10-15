# House Architecture

A portable, instruction-only skill for organizing systems around independently owned capabilities, shared specialists, and a verified integration path.

## Install

From this repository root, run the following after cloning or downloading the repository. It refuses to replace an existing skill directory or symlink.

```sh
target="${CODEX_HOME:-$HOME/.codex}/skills/house-architecture"
if [ -e "$target" ] || [ -L "$target" ]; then
  printf 'Refusing to overwrite existing path: %s\n' "$target" >&2
  exit 1
fi
mkdir -p "$(dirname "$target")"
cp -R "skills/house-architecture" "$target"
```

## Use

Invoke the installed skill with **`$house-architecture`**. Describe the person-facing outcome, existing boundaries and owners, current constraints, and the evidence needed for a usable result.

Read [the skill instructions](skills/house-architecture/SKILL.md). The example is conceptual. This package provides design guidance, not a runtime, organization, or proof that a system has been integrated or accepted. Installation does not prove that a host loaded the skill.

## License

MIT. See [LICENSE](LICENSE).
