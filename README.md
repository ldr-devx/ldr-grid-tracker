
# Habit Grid Tracker

An Obsidian plugin that visualizes your daily habit progress using GitHub-style grids.

![Obsidian](https://img.shields.io/badge/Obsidian-Plugin-7c3aed)
![License](https://img.shields.io/badge/License-MIT-green)

## Features

- Habit visualization with GitHub contribution-style grids  
- Customizable colors for each habit  
- Streak, total, and weekly progress statistics  
- Real-time updates when the file is modified  
- Compatible with light and dark themes  

## Installation

### Manual Installation

1. Download the files `main.js`, `manifest.json`, and `styles.css`
2. Create a folder named `habit-grid-tracker` in your vault: `.obsidian/plugins/habit-grid-tracker/`
3. Copy the downloaded files into that folder
4. Restart Obsidian
5. Go to Settings → Community Plugins → Enable "Habit Grid Tracker"

### Development

```bash
# Clone the repository
git clone https://github.com/your-username/habit-grid-tracker.git
cd habit-grid-tracker

# Install dependencies
npm install

# Build in development mode (with hot reload)
npm run dev

# Build for production
npm run build
````

## Usage

### 1. Create the habits file

Create a Markdown file in your vault (e.g. `_habits/2026.md`) with the following format:

```markdown

    # Grids
    
    ```habit-definition
    tema: estudio
    emoji: 📚
    colors: ["#ebedf0", "#c4b5fd", "#a78bfa", "#8b5cf6", "#7c3aed"]
    meta_semanal: 5
    descripcion: Study at least 1 hour
    ```
    
    ```habit-definition
    tema: ejercicio
    emoji: 💪
    colors: ["#ebedf0", "#fca5a5", "#f87171", "#ef4444", "#dc2626"]
    meta_semanal: 6
    descripcion: Physical activity for 30+ minutes
    ```
    
    # TODO list
    
    ## 01/01/2026
    
    * [x] estudio
    * [x] ejercicio
    
    ## 02/01/2026
    
    * [x] estudio
    * [ ] ejercicio



```

### 2. Configure the plugin

1. Go to Settings → Habit Grid Tracker
2. Enter the path to your habits file
3. Done

### 3. Open the view

- Click the new icon in the left sidebar
- Or use the command: `Habit Grid: Open Habit Grid view`

## File Format

### Habit Definition

Each habit is defined inside a code block with `habit-definition`:

| Property | Required | Description |
|----------|----------|-------------|
| `tema` | Yes | Unique habit name |
| `emoji` | No | Representative emoji |
| `colors` | No | Color array (min 2, max 5) |
| `meta_semanal` | No | Target days per week (default: 7) |
| `descripcion` | No | Habit description |
| `grupo` | No | Used to group related habits |

### Task List

The `# TODO list` section contains daily entries:

- Each day is marked with `## DD/MM/YYYY`
- Habits are marked with checkboxes: `- [ ]` (not done) or `- [x]` (done)
- The checkbox name must match exactly the defined `tema`

## Configuration

| Option | Description |
|-------|-------------|
| File path | Path to the habits file |
| Show statistics | Show or hide statistics |
| Week starts on | Monday or Sunday |
| Cell size | Cell size in px (8–20) |
| Cell spacing | Spacing between cells in px (1–6) |

## Suggested Color Palettes

### Green (GitHub style)
```

["#ebedf0", "#9be9a8", "#40c463", "#30a14e", "#216e39"]

```

### Purple
```

["#ebedf0", "#c4b5fd", "#a78bfa", "#8b5cf6", "#7c3aed"]

```

### Red
```

["#ebedf0", "#fca5a5", "#f87171", "#ef4444", "#dc2626"]

```

### Blue
```

["#ebedf0", "#93c5fd", "#60a5fa", "#3b82f6", "#2563eb"]

```

### Orange
```

["#ebedf0", "#fdba74", "#fb923c", "#f97316", "#ea580c"]

```

## Commands

| Command | Description |
|--------|-------------|
| `Habit Grid: Open view` | Opens the visualization panel |
| `Habit Grid: Refresh data` | Reloads data from the file |

## License

MIT License – see [LICENSE](LICENSE) for more details.

## Contributing

Contributions are welcome. Please open an issue or pull request.

---

Made for the Obsidian community
