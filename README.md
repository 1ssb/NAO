# NAO

This repository contains the NAO project with the NAO-bot-documentation as a submodule.

## Submodule Setup

The `NAO-bot-documentation` is included as a git submodule to keep documentation synchronized with the main project.

### Initial Setup

If you're cloning this repository for the first time, use:
```bash
git clone --recursive https://github.com/1ssb/NAO.git
```

### Working with Submodules

#### Pulling Latest Changes
To get the latest changes from the submodule:
```bash
git submodule update --remote --merge
```

#### Making Changes in the Submodule
1. Navigate to the submodule directory:
   ```bash
   cd NAO-bot-documentation
   ```

2. Make your changes, then commit and push:
   ```bash
   git add .
   git commit -m "Your commit message"
   git push origin main
   ```

3. Return to the main repository and update the submodule reference:
   ```bash
   cd ..
   git add NAO-bot-documentation
   git commit -m "Update submodule to latest"
   ```

#### Updating Existing Clones
If you already have this repository cloned, update it with:
```bash
git pull
git submodule update --init --recursive
```

### Repository Structure
```
NAO/
├── README.md
├── .gitmodules
└── NAO-bot-documentation/  # Submodule
    └── [documentation files]
```

## Development Workflow

1. Always pull latest changes before starting work
2. Make changes in the appropriate repository (main or submodule)
3. Commit and push changes in the correct order
4. Keep submodules updated to latest versions

## Troubleshooting

If you encounter submodule issues:
```bash
# Reinitialize submodules
git submodule deinit -f NAO-bot-documentation
git submodule update --init --recursive

# Or reset to a clean state
git submodule foreach git reset --hard
git submodule update --init --recursive
```
