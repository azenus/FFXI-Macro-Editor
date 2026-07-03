# ZenithXI Macro Editor — User Guide

A Windows desktop tool for editing your **Final Fantasy XI** macros outside the game.
It reads and writes the game's macro files directly, so you can organize your macros
into books and sets, edit them with a full keyboard, insert auto-translate phrases, and
back up (and restore) every character's macros.

## Table of Contents
1. Introduction
2. Getting Started
3. Interface Overview
4. Basic Operations
5. Managing Macro Sets and Books
6. Backup and Restore
7. Advanced Features
8. Tips and Tricks

---

## 1. Introduction

The ZenithXI Macro Editor helps Final Fantasy XI players manage their in-game macros more
efficiently. It lets you edit macros outside the game, organize them into sets and books,
switch between characters, and create (and restore) backups of your macro configurations.

Every macro layout the game supports is available:

- **40 macro books**, each with **10 sets**
- **20 macros per set** — 10 **Ctrl** macros and 10 **Alt** macros
- Each macro has a **name** and **6 command lines**

## 2. Getting Started

### Installation and First Launch
- On launch, the editor automatically detects your FFXI installation and loads your
  character's macro files.
- It reads the in-game name for each character and lists everyone it finds in the
  **Character** dropdown.
- If automatic detection fails, open **File → Preferences** to set your game region
  (NA / EU / JP) or point the editor at a custom macro folder. You can also use
  **File → Open** to open a macro file directly.
- If any macro files don't exist yet, the editor creates the necessary files for you.

### Selecting a Character
- Use the **Character** dropdown at the top of the left panel to switch between characters.
- Selecting a character loads their macros starting at Book 1 / Set 1. If you have unsaved
  changes, you'll be prompted to save first.

### Opening Macro Files Manually
1. Click **File → Open**.
2. Navigate to your character's folder (usually under the FFXI `USER` directory).
3. Select any macro (`.dat`) file to begin editing.

## 3. Interface Overview

### Title Bar and Menus (top)
- **File** — Open, Save, Preferences, Backup Macros, Restore Macros, Exit
- **Edit** — Cut / Copy / Paste / Delete, plus **Macro Book** and **Individual Macro**
  submenus and **Insert Auto-Translate…**
- **Options** — toggle the **Single Macro Line Text Box** editing mode
- Window controls (minimize / maximize / close) sit at the right.

### Left Panel
- **Macro Book card** — the current book's name (editable) and set navigation
  (◄ / ► buttons with a "Set X/10" indicator).
- **Character card** — the **Character** dropdown and a tree view of all books and sets for
  the selected character. Books are numbered 1–40, each containing 10 sets.

### Right Panel
- **Macro Slots card** — the **Ctrl Macros** (1–10) and **Alt Macros** (1–10) buttons.
  Click a slot to load it into the editor below.
- **Macro Editor card** — edit the selected macro:
  - Quick actions: **+ Auto-Translate**, **Copy**, **Paste**, **Clear**
  - **Name** field (up to 8 characters)
  - **6 command lines** (or a single multi-line box in single-line mode)

### Status Bar
- Displays current operations and status messages at the bottom of the window.

## 4. Basic Operations

### Editing Macros
1. Select a macro by clicking its **Ctrl** or **Alt** slot button.
2. Edit the macro name in the **Name** field.
3. Enter your commands in the six line fields.
4. Changes are tracked automatically but must be **saved manually**.

### Saving Changes
- Click **File → Save** or press **Ctrl+S**.
- The editor writes the macro file and recalculates its MD5 hash so the game accepts it.
- Saves are written safely (to a temporary file, then swapped into place).

### Copying, Pasting, and Clearing Macros
- **Right-click any macro slot button** for a context menu: **Copy Macro**, **Paste Macro**,
  **Clear Macro**.
- The **Copy / Paste / Clear** buttons in the Macro Editor act on the currently selected
  macro, and the **Edit** menu offers the same actions.
- Keyboard shortcuts:

| Action           | Shortcut         |
|------------------|------------------|
| Save             | `Ctrl+S`         |
| Copy macro       | `Alt+C`          |
| Paste macro      | `Alt+V`          |
| Clear macro      | `Alt+Delete`     |
| Copy book set    | `Ctrl+Shift+C`   |
| Paste book set   | `Ctrl+Shift+V`   |
| Insert auto-translate | `Ctrl+T`    |

### Inserting Auto-Translate Phrases
1. Place your cursor where you want the phrase, then click **+ Auto-Translate** (or press
   **Ctrl+T**, or use **Edit → Insert Auto-Translate…**).
2. Search for and select a phrase to insert it into the macro line.
- Auto-translate phrases (and special icons) take up more space than plain text, so a line
  containing them holds fewer characters.

## 5. Managing Macro Sets and Books

### Navigating Sets
- Use the **◄ / ►** buttons beside the set indicator to move between sets.
- Each book has 10 sets; the current one is shown as **"Set X/10"**.

### Renaming Books
1. Click the book-name field at the top of the left panel.
2. Type the new name (up to 16 characters).
3. The name is saved automatically when you click away.

### Switching Books and Characters
- Use the **tree view** on the left to jump to any book or set.
- Use the **Character** dropdown to switch characters.
- Right-click a character in the tree and choose **Edit Display Name** to give it a custom
  label (useful when the folder ID isn't recognizable).

## 6. Backup and Restore

### Creating Backups
- Click **File → Backup Macros**.
- The editor backs up **every character** it finds — one ZIP archive per character. Each
  archive contains that character's macro files (`mcr*.dat`) and book names
  (`mcr.ttl` / `mcr_2.ttl`).
- Backups are stored in a **`Backups`** folder next to the application, named
  `MacroBackup_{characterId}_{timestamp}.zip`.
- The editor keeps the **10 most recent backups per character** and removes older ones.

### Restoring Backups
1. Click **File → Restore Macros…**.
2. Choose a backup from the list — each row shows the **character name** and the
   **date/time** the backup was made.
3. Click **Restore** and confirm.
- Before overwriting, the editor automatically makes a fresh backup of the current macros,
  so a restore can itself be undone.
- The backup is restored to the character it originally belonged to. If that character's
  folder isn't found, you can choose to restore into the currently loaded character instead.

> **Close FFXI before restoring.** The game can keep macro files open; if a file is locked,
> the editor will tell you which files it couldn't restore so you can close the game and
> try again.

## 7. Advanced Features

### Multi-Character Support
- The editor manages macros for all characters under your FFXI `USER` folder.
- Switch between them with the **Character** dropdown; each character's in-game name is read
  automatically, and custom display names are remembered.

### Preferences (File → Preferences)
- **Game Region** — NA, EU, or JP, used to locate the correct installation.
- **Custom Folder Override** — point the editor at a specific macro folder if auto-detection
  doesn't find your install.

### Single-Line Editing Mode
- Toggle **Options → Single Macro Line Text Box** to switch between six individual line
  fields and a single multi-line box for faster editing.

## 8. Tips and Tricks

### Efficient Macro Management
- Use descriptive names for macros and books to stay organized.
- Create a backup before making major changes.
- Use copy/paste to duplicate commonly used macro structures.
- Save your changes before switching between macros, sets, or characters.

### Character Limits
- **Macro names:** 8 characters
- **Macro lines:** up to 60 characters each (fewer if the line includes auto-translate
  phrases or special icons)
- **Book names:** 16 characters

### File Organization
- Main macro file: `mcr.dat`
- Numbered files: `mcr1.dat` through `mcr399.dat` (40 books × 10 sets)
- Book names: `mcr.ttl` (books 1–20) and `mcr_2.ttl` (books 21–40)

### Best Practices
- Back up regularly — and always before a big reorganization.
- Use clear, consistent naming so macros are easy to identify.
- Test macros in-game after making significant changes.
- Keep related macros together in the same set.
- Close the FFXI client before saving or restoring so macro files aren't locked.
