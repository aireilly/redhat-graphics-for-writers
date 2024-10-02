# Red Hat Diagrams in SVG

Develop SVG source files in the `source/` folder, get the optimized SVG from the `for-web/` folder.

## Optimize SVG files

> ! These instructions are written for Linux and Mac

Install Node JS on your system: https://nodejs.org/en/download/

Then open a terminal window, navigate to this folder and run:
```cmd
npm install
```

This installs the tools needed to optimize the SVGs

### Enabling automatic SVG optimization
To enable SVG optimization on every git commit run these two commands in this folder from the terminal:

```cmd
cp .git-hooks/* .git/hooks/
chmod +x .git/hooks/*
```

This adds some commands that will run pre and post git commit to automatically optimize the SVG files.

### Running SVG optimization manually
Run this command at any time to optimize all of the SVG files in the `source/` folder, the result will be added to `for-web/`:

```cmd
npm run build
```

### TODO

inkscape settings!

1. Set SVG 1.1 compatible
2. Set 1px grid in prefs, and snap to grid for all objects
3. PNG output prefs: DPI 96, Best compression, anitalias 3, RGBA 8
