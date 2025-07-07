# Ro Shambo: Dungeon of Hands

A roguelike deck-builder game with advanced Rock-Paper-Scissors combat mechanics, built in Godot 4.x.

## 🎮 Game Overview

**Ro Shambo: Dungeon of Hands** is a strategic card game where you explore procedurally generated dungeons, battle enemies using an evolved Rock-Paper-Scissors system, and build your deck with powerful gesture cards.

### Core Mechanics

- **Advanced RPS Combat**: Turn-based battles using Rock, Paper, Scissors with special variants and effects
- **Deck Building**: Collect and upgrade gesture cards with unique abilities
- **Roguelike Progression**: Permadeath runs with unlockable content
- **Procedural Dungeons**: Each run features different room layouts and encounters

## 🚀 Getting Started

### Prerequisites

- Godot 4.2 or later
- No additional dependencies required

### Installation

1. Clone or download this repository
2. Open Godot 4.x
3. Click "Import" and select the project folder
4. Click "Import & Edit"
5. Press F5 or click the "Play" button to run the game

## 🎯 How to Play

### Basic Controls

- **Mouse**: Click to select cards and interact with UI
- **Enter/Space**: Confirm selections
- **Escape**: Cancel/go back

### Game Flow

1. **Start a Run**: Click "Start Game" from the main menu
2. **Explore Dungeon**: Navigate through rooms on the dungeon map
3. **Enter Rooms**: Click "Enter Room" to engage with the room's content
4. **Combat**: Play gesture cards to defeat enemies
5. **Progress**: Complete floors to advance deeper into the dungeon

### Combat System

#### Turn Structure
- **Player Turn**: Draw 3 cards, play 1 card
- **Enemy Turn**: Enemy chooses and reveals their gesture
- **Resolution**: Compare gestures using RPS rules
  - **Win**: Deal damage to enemy
  - **Lose**: Take damage from enemy
  - **Tie**: Gain charge meter

#### Gesture Types
- **Rock (✊)**: Beats Scissors, loses to Paper
- **Paper (✋)**: Beats Rock, loses to Scissors  
- **Scissors (✌️)**: Beats Paper, loses to Rock

#### Card Effects
- **Damage**: Base damage dealt on successful hits
- **Effects**: Special abilities like DoT, Block, Draw, etc.
- **Cooldowns**: Some cards can't be used for several turns after playing

### Room Types

- **⚔️ Combat**: Battle enemies for rewards
- **👹 Mini-Boss**: Tougher enemies with better rewards
- **💀 Boss**: Final challenge of each floor
- **🏕️ Rest**: Heal HP and remove cards
- **❓ Event**: Random encounters with various outcomes
- **💰 Shop**: Purchase and upgrade cards

### Strategy Tips

1. **Build Synergy**: Combine cards that work well together
2. **Manage Resources**: Balance HP, gold, and card upgrades
3. **Learn Patterns**: Study enemy AI patterns to predict their moves
4. **Plan Ahead**: Consider cooldowns and card draw when building your deck

## 🛠️ Development

### Project Structure

```
GameDev3/
├── scripts/           # Game logic and systems
│   ├── Card.gd       # Card class and gesture types
│   ├── Deck.gd       # Deck management
│   ├── Enemy.gd      # Enemy AI and stats
│   ├── CombatManager.gd # Combat system
│   ├── GameManager.gd # Overall game flow
│   └── ...
├── scenes/           # Godot scene files
│   ├── Main.tscn    # Main game scene
│   └── CardDisplay.tscn # Card UI component
└── project.godot    # Godot project configuration
```

### Key Systems

- **Card System**: Data-driven cards with effects and cooldowns
- **Combat Engine**: Turn-based RPS with gesture resolution
- **Dungeon Generation**: Procedural room layouts and encounters
- **AI System**: Pattern-based and weighted random enemy behavior
- **UI Framework**: Modular interface components

### Extending the Game

#### Adding New Cards
1. Modify `CardDatabase.gd` to add new card definitions
2. Update card effects in the `Card` class
3. Add visual styling in `CardDisplay.gd`

#### Adding New Enemies
1. Create enemy definitions in `EnemyDatabase.gd`
2. Define AI patterns and stats
3. Set up rewards and drops

#### Adding New Room Types
1. Extend `DungeonGenerator.RoomType` enum
2. Add room creation logic in `DungeonGenerator.gd`
3. Implement room behavior in `GameManager.gd`

## 🎨 Art and Assets

This prototype uses:
- **Text-based UI**: Clean, readable interface
- **Unicode Symbols**: Gesture representations (✊✋✌️)
- **Color Coding**: Visual feedback for different gesture types
- **Minimal Design**: Focus on gameplay over graphics

## 📝 Design Document

The game is based on a comprehensive design document that includes:
- Core game loop and mechanics
- Card system specifications
- Enemy AI patterns
- Dungeon generation rules
- Progression systems

## 🤝 Contributing

This is a prototype implementation. Feel free to:
- Report bugs or issues
- Suggest improvements
- Fork and extend the game
- Create mods or variants

## 📄 License

This project is open source. Feel free to use, modify, and distribute as you see fit.

## 🎯 Future Development

Potential areas for expansion:
- More card types and effects
- Additional enemy types and AI patterns
- Expanded dungeon generation
- Visual improvements and animations
- Sound effects and music
- Save/load system
- Achievement system
- Multiplayer features

## UI Layout & Design

The main game screen is designed for clarity and usability:

- **Energy Label**: Top left. Shows current energy (e.g., 'Energy: 3').
- **Charge Bar**: Below energy. Shows charge meter (0-5). Use a TextureProgressBar with a clear fill color.
- **Hand Container**: Bottom center. HBoxContainer holding CardDisplay scenes for each card in hand. Cards are spaced evenly.
- **Potion Bar**: Bottom right. Shows potion inventory. Each potion is a button with a tooltip and use effect.
- **View Deck Button**: Top right. Opens a popup to view the player's deck.

**Tips for Godot UI:**
- Use anchors and margins for responsive layout.
- Use containers (HBox, VBox, Grid) for dynamic elements like hand and potion bar.
- Avoid overlap by spacing UI elements and using the editor's layout tools.
- Use clear, readable fonts and icons.
- Group related UI elements (energy/charge, hand, potions) for intuitive access.

See `CombatUI.gd` for node names and setup comments.

---

**Enjoy playing Ro Shambo: Dungeon of Hands!** 🎮✊✋✌️ 