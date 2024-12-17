# FFXI Macro Editor User Guide

## Table of Contents
1. Introduction
2. Getting Started
3. Interface Overview
4. Basic Operations
5. Managing Macro Sets
6. Advanced Features
7. Tips and Tricks

## 1. Introduction

The FFXI Macro Editor is a tool designed to help Final Fantasy XI players manage their in-game macros more efficiently. It allows you to edit macros outside the game, organize them into sets and books, and create backups of your macro configurations.

## 2. Getting Started

### Installation and First Launch
- The program will automatically detect your FFXI installation directory and locate your character's macro files
- If the automatic detection fails, you can manually open macro files through the File menu
- The editor will create necessary macro files if they don't exist

### Opening Macro Files
1. Click "File" → "Open"
2. Navigate to your character's folder (usually found in the FFXI USER directory)
3. Select any macro (.dat) file to begin editing

## 3. Interface Overview

The interface is divided into several sections:

### Left Panel
- Displays a tree view of all macro books and sets
- Organized by character name and then by books (1-40)
- Each book contains 10 sets of macros

### Right Panel
#### Top Section
- Book name display and editor
- Set navigation controls (Previous/Next buttons)

#### Middle Section
- Ctrl Macros (10 buttons for macros 1-10)
- Alt Macros (10 buttons for macros 1-10)

#### Bottom Section
- Macro editor with fields for:
  - Macro name (max 8 characters)
  - 6 macro lines (max 255 characters each)

### Status Bar
- Displays current operations and status messages

## 4. Basic Operations

### Editing Macros
1. Select a macro by clicking its corresponding Ctrl or Alt button
2. Edit the macro name in the "Name" field
3. Enter macro commands in the six line fields
4. Changes are automatically tracked but must be saved manually

### Saving Changes
- Click "File" → "Save" or use the keyboard shortcut
- The program will update the macro file and recalculate the MD5 hash

### Copying and Pasting Macros
- Right-click any macro button to access the context menu
- Options include:
  - Copy Macro
  - Paste Macro
  - Clear Macro
- You can also use the Edit menu for the currently selected macro

## 5. Managing Macro Sets

### Navigating Sets
- Use the arrow buttons beside the set number to move between sets
- Each book contains 10 sets
- The current set number is displayed in the format "Set X/10"

### Renaming Books
1. Click the book name field at the top of the right panel
2. Enter the new name (max 16 characters)
3. The name is saved automatically when you click away

### Switching Books
- Use the tree view on the left to switch between different macro books
- Books are numbered 1-40 with customizable names

## 6. Advanced Features

### Backup System
- Access through "File" → "Backup Macros"
- Creates a ZIP file containing all macro data
- Backup includes:
  - All macro .dat files
  - Book names (mcr.ttl files)
- Backups are stored in the application's Backup folder
- The system maintains the 10 most recent backups

### Multi-Character Support
- Can manage macros for multiple characters
- Character folders are displayed in the tree view
- Switch between characters by selecting different folders

## 7. Tips and Tricks

### Efficient Macro Management
- Use descriptive names for macros and books to stay organized
- Create backups before making major changes
- Use copy/paste to duplicate commonly used macro structures
- Remember to save changes before switching between macro files

### Character Limits
- Macro names: 8 characters
- Macro lines: 255 characters
- Book names: 16 characters

### File Organization
- Main macro file: mcr.dat
- Numbered files: mcr1.dat through mcr399.dat
- Book names: mcr.ttl and mcr_2.ttl

### Best Practices
- Create regular backups of your macros
- Use clear naming conventions for easy identification
- Test macros in-game after making significant changes
- Keep related macros in the same set for better organization

