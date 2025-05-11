## Overview
This is my Firefox custom theme that gives your browser tabs a cyberpunk aesthetic with neon colored borders for selected tabs. Each tab cycles through a vibrant cyberpunk color palette, creating a unique and visually striking browsing experience.

## Features
- Custom tab styling with subtle background coloring and unique border-radius
- Vibrant cyberpunk color palette for selected tabs
- 14 distinct neon colors that cycle through tabs
- Streamlined menu styling with reduced padding for a cleaner look

## Installation

### Prerequisites
- Firefox browser (works with recent versions)
- Access to your Firefox profile folder

### Step-by-step installation
1. Find your Firefox profile folder:
   - Open Firefox and enter `about:support` in the address bar
   - Look for "Profile Folder" and click "Open Folder" or "Show in Finder"

2. Create a chrome folder (if it doesn't exist):
   - Inside your profile folder, create a folder named `chrome`

3. Install the theme:
   - Create a new file called userChrome.css inside the chrome folder
   - Copy all the CSS code from this repository into that file
   - Save the file

4. Enable custom CSS in Firefox:
   - Enter `about:config` in the address bar
   - Search for `toolkit.legacyUserProfileCustomizations.stylesheets`
   - Set it to `true` by double-clicking it

5. Restart Firefox for changes to take effect

## How It Works

### Tab Styling
The theme applies a subtle background color to all tabs with a unique border-radius that gives them a slightly edgy appearance.

```css
.tab-background {
  border-radius: 2px 0px 2px 0px !important;
  margin-bottom: 0px !important;
  background-color: color-mix(in srgb, currentColor 5%, transparent);
  border-top: 2px solid rgba(255, 255, 255, 0.1) !important;
}
```

### Cyberpunk Color System
The theme defines a set of 14 vibrant neon colors in the cyberpunk palette:

- Neon Pink (#ff00c3)
- Electric Cyan (#00ffff)
- Deep Purple (#ae00ff)
- Toxic Green (#09ff00)
- Neon Orange (#ff8800)
- Laser Red (#ff0037)
- Volt Yellow (#d9ff00)
- Hot Red (#ff4444)
- Alien Green (#aaff00)
- Molten Orange (#ff5100)
- Digital Blue (#01cdfe)
- Synthwave Green (#05ffa1)
- Ultraviolet (#b967ff)
- Electric Yellow (#fffb96)

Each tab gets assigned a color based on its position, cycling through the palette using the `nth-of-type` selector.

### Menu Optimization
The theme reduces padding in context menus and panel menus for a more compact interface:

```css
menupopup > menu,
menupopup > menuitem {
  padding-block: 2px !important;
}

:root {
  --arrowpanel-menuitem-padding: 2px !important;
}
```

## Customization
You can easily modify the theme by:
- Changing the colors in the `--cyberpunk-colors` variable
- Adjusting tab border thickness or radius
- Modifying menu padding values

## Troubleshooting
- If styles are not applied after installation, verify that `toolkit.legacyUserProfileCustomizations.stylesheets` is set to `true`
- If updates to the CSS don't apply, try clearing Firefox's cache and restarting
- Make sure the file path is correct: it should be in `[profile folder]/chrome/userChrome.css`
