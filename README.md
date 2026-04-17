# Nomad

A game built with the [Moonshot](https://github.com/jfraper/moonshot) engine.

## Quick Start

```bash
# Clone the repo
git clone https://github.com/jfraper/nomad
cd nomad

# Initialize the engine submodule
git submodule update --init --recursive

# Build and run
./scripts/build.sh --run
```

## Scripts

| Command | Description |
|---------|-------------|
| `./scripts/build.sh --run` | Debug build and run (with hot reload) |
| `./scripts/build.sh --release --run` | Release build and run |
| `./scripts/build.sh --clean --run` | Clean rebuild |
| `./scripts/build.sh --update-engine` | Update engine to latest version |
| `./scripts/run.sh` | Run last build |
| `./scripts/run.sh --release` | Run last release build |

## Project Structure

```
nomad/
  engine/          # Moonshot engine (git submodule)
  src/
    main.cpp       # Game entry point
  assets/          # Game assets (textures, sounds, etc.)
  scripts/         # Build and run scripts
  dist/            # Build output (auto-generated)
```

## Updating the Engine

```bash
# Update to latest engine
./scripts/build.sh --update-engine


# Or pin to a specific version
cd engine
git checkout v0.18.0
cd ..
git add engine
git commit -m "pin engine to v0.18.0"
```


