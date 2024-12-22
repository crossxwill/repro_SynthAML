# Repro SynthAML

## Requirements

1. Install Miniforge (package manager): https://github.com/conda-forge/miniforge

2. Install VS Code (IDE): https://code.visualstudio.com

3. Install Git: https://git-scm.com

4. Install GitHub Desktop: https://github.com/apps/desktop

## Install Python Environment

1. Create the conda environment from the `environment.yml` file:

```sh
mamba env create -f environment.yml
```

2. Activate the conda environment:

```sh
mamba activate env_AutoGluon_202412
```

3. Launch VS Code:

```sh
code
```

## Import VS Code Settings (on Windows)

1. Import VS code extensions:

```sh
FOR /F "usebackq tokens=*" %A IN (".\\.vscode\\vscode_extensions.txt") DO code --install-extension %A
```

2. Import VS code settings:

```sh
copy /Y .\\.vscode\\vscode_settings.json "%APPDATA%\\Code\\User\\settings.json"
```

3. Import VS code keybindings:

```sh
copy /Y .\\.vscode\\vscode_keybindings.json "%APPDATA%\\Code\\User\\keybindings.json"
```