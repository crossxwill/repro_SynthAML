# Repro SynthAML

## Pre-requisites

1. Install Miniforge (package manager): https://github.com/conda-forge/miniforge

2. Install VS Code (IDE): https://code.visualstudio.com

3. Install Git: https://git-scm.com

4. Install GitHub Desktop: https://github.com/apps/desktop

## Clone the Repository

1. Open GitHub Desktop (and link your GitHub account).
2. Click on `File` > `Clone Repository...`.
3. Select the `URL` tab.
4. Enter the URL of the repository: `https://github.com/crossxwill/repro_SynthAML`
5. Click on `Choose...` and select the directory where you want to save the repository.
6. Click on `Clone`.

## Install Python Environment

1. Click the `Start` button.
2. Search for `Miniforge Prompt`.
3. Change the directory to the repository (see Step 5)
4. Create the conda environment from the `environment.yml` file:

```bash
mamba env create -f environment.yml
```

5. Activate the conda environment:

```bash
mamba activate env_AutoGluon_202412
```

6. Launch VS Code:

```bash
code
```

## Import VS Code Settings (using Windows Command Prompt - not PowerShell)

1. Import VS code extensions:

```bash
FOR /F "usebackq tokens=*" %A IN (".\\.vscode\\vscode_extensions.txt") DO code --install-extension %A
```

2. Import VS code settings:

```bash
copy /Y .\\.vscode\\vscode_settings.json "%APPDATA%\\Code\\User\\settings.json"
```

3. Import VS code keybindings:

```bash
copy /Y .\\.vscode\\vscode_keybindings.json "%APPDATA%\\Code\\User\\keybindings.json"
```