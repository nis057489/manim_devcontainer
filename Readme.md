# Manim Dev Container

Quickly get up and running with [Manim](https://docs.manim.community/en/stable/index.html) in a Docker-based development environment. This repository includes a `.devcontainer/devcontainer.json` configuration for Visual Studio Code, using the official [Manim Community Docker image](https://hub.docker.com/r/manimcommunity/manim).

---

## Quick Start

1. **Install VS Code and Extensions**  
   - Make sure you have [Visual Studio Code](https://code.visualstudio.com/) installed.
   - Install the **Remote - Containers** extension (or **Dev Containers** extension in newer versions).

2. **Open the Project in a Dev Container**  
   - Clone or download this repository.
   - Launch VS Code and open this folder.
   - When prompted, or by opening the Command Palette (`Ctrl + Shift + P` or `Cmd + Shift + P`), select:
     > **Dev Containers: Open Folder in Container...**
   - VS Code will build the environment using the `devcontainer.json` file.

3. **Start Using Manim**  
   - Once the container starts, open a new terminal in VS Code (inside the container).
   - (Recommended) Use the Command Palette (`Ctrl + Shift + P` or `Cmd + Shift + P`) to invoke Manim commands provided by the [Manim Extension](https://github.com/Rickaym/manim-sideview?tab=readme-ov-file#getting-started)
   - The most useful ones are probably `Runs a Side View`, `Render a new Scene`, and `Show Internal Manim Config`
   - (Alternatively) Run Manim commands as needed, for example:
     ```bash
     manim example_scenes.py SquareToCircle -p -ql
     ```
   - Your rendered videos and/or images will be saved inside your local project folder.

---

## Documentation

- **Manim SideView Extension**  
  - [GitHub: manim-sideview](https://github.com/Rickaym/manim-sideview)  
  - An extension that lets you preview your Manim animations directly in VS Code.

- **Manim Community Documentation**  
  1. [Getting Started and Examples](https://docs.manim.community/en/stable/examples.html)  
  2. [Main Documentation](https://docs.manim.community/en/stable/index.html)  

Check out these links for tutorials and advanced usage examples.

---

## Customising the Dev Container

- **Install Additional Python Packages**: Modify the `postCreateCommand` in `.devcontainer/devcontainer.json` or create a `requirements.txt`.
- **Use a Custom Dockerfile**: Replace `"image": "manimcommunity/manim:stable"` with a `"dockerFile": "Dockerfile"` and customise as you see fit.
- **Add More VS Code Extensions**: In `.devcontainer/devcontainer.json`, add to the `"extensions"` array inside `customizations`.
