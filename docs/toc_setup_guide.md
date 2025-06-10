# Jupyter Notebook TOC Generator Setup Guide

## Overview
This guide explains how to install and use a custom Table of Contents (TOC) generator for Jupyter notebooks that:
- Adds a toolbar button and menu item to Jupyter
- Automatically generates TOC from notebook headers
- Updates TOC in-place within the notebook
- Works with the GitHub markdown conversion workflow

## Prerequisites

### 1. TOC Generation Script
First, ensure you have the TOC generation script in your project:

**Location:** `scripts/generate_toc.py`

This Python script:
- Scans notebook for markdown headers
- Generates formatted TOC with links
- Updates TOC in cells marked with `<!-- TOC -->`

### 2. Project Structure
```
your-project/
├── scripts/
│   └── generate_toc.py
├── notebooks/
│   └── your_notebooks.ipynb
└── .github/
    └── workflows/
        └── mermaid.yml
```

## Installation Steps

### Step 1: Create Extension Directory
```bash
mkdir -p ~/.jupyter/nbextensions/toc_generator
```

### Step 2: Create Extension File
Save the JavaScript extension code as:
```
~/.jupyter/nbextensions/toc_generator/main.js
```

### Step 3: Install Extension
```bash
jupyter nbextension install ~/.jupyter/nbextensions/toc_generator --user
```

### Step 4: Enable Extension
```bash
jupyter nbextension enable toc_generator/main --user
```

### Step 5: Restart Jupyter
Close and restart your Jupyter notebook server.

## Usage

### 1. Add TOC Marker
In your notebook, create a markdown cell with:
```markdown
<!-- TOC -->
```

This marks where the table of contents will be generated.

### 2. Generate TOC
After restarting Jupyter:
- Click the list icon (📋) in the toolbar, OR
- Use Insert menu → Generate Table of Contents

### 3. Save and Reload
- The extension updates the notebook file
- Save the notebook (Ctrl+S)
- Reload the page to see the updated TOC

## How It Works

1. **Button Click:** Triggers the extension's JavaScript function
2. **Python Execution:** Runs `scripts/generate_toc.py` via kernel
3. **File Update:** Script modifies the .ipynb file directly
4. **User Notification:** Dialog shows success/error message

## Integration with GitHub Workflow

The generated TOC:
- Uses markdown anchor links `[Section](#section)`
- Links work in GitHub after conversion
- Compatible with the mermaid.yml workflow
- Maintains proper formatting in both environments

## Troubleshooting

### "No TOC marker found"
Add a markdown cell with `<!-- TOC -->` where you want the TOC.

### "Error generating TOC"
Ensure:
- `scripts/generate_toc.py` exists in your project
- You're running Jupyter from the project root
- The notebook is saved before generating TOC

### Button doesn't appear
- Verify extension is enabled: `jupyter nbextension list`
- Check browser console for JavaScript errors
- Try hard refresh (Ctrl+Shift+R)

## Notes

- TOC links navigate to sections in GitHub markdown
- In Jupyter, links display but don't jump (Jupyter limitation)
- Cell numbers in TOC help manual navigation in Jupyter
- Always pull changes after GitHub Actions runs to sync .md files