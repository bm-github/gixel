# Git Pattern Generator

Git Pattern Generator is a web-based tool that allows you to create custom contribution patterns for your Git commit history. You can design pixel-art-like patterns that will appear in your GitHub contribution graph by generating backdated commits.

## Features

- Interactive grid interface matching GitHub's contribution graph
- 5-level intensity control per cell (matching GitHub's contribution heat levels)
- Date-aware grid that adjusts for the starting and ending days of the selected year
- Generates a bash script for creating the commit pattern
- Supports any year input
- Hover tooltips showing the exact date for each cell

## Usage

1. Open `gixel.html` in your web browser
2. Select the desired year using the input field
3. Click on cells in the grid to cycle through intensity levels:
   - Level 0 (Gray): No commits
   - Level 1 (Light green): 1 commit
   - Level 2 (Medium green): 2 commits
   - Level 3 (Darker green): 3 commits
   - Level 4 (Darkest green): 4 commits
4. Click "Generate Script" to create the bash script
5. Either:
   - Click "Copy to Clipboard" to copy the script
   - Click "Download Script" to download as `gixel-commits.sh`

## Running the Generated Script

1. Make the script executable:
```bash
chmod +x gixel-commits.sh
```

2. Run the script in your Git repository:
```bash
./gixel-commits.sh
```

3. To remove the gixel art just delete the repo. Likewise, to change it then delete then push a newscript.

![example](/example.png)

Note: The script creates empty commits with backdated timestamps. Make sure you're in the correct Git repository before running the script.


## Technical Details

- The tool generates empty commits using `git commit --allow-empty`
- Each commit is timestamped with random times between 9:00 AM and 8:59 PM
- Commits are dated according to the selected pattern
- The script automatically pushes changes to the 'main' branch

## Styling

The interface matches GitHub's dark theme with:
- Dark background (#0d1117)
- GitHub-style fonts
- Contribution graph colors matching GitHub's scheme
- Responsive grid layout
- Hover effects on interactive elements

## Browser Compatibility

The tool uses modern JavaScript features and should work in all recent versions of major browsers. Required features include:
- CSS Grid
- Flexbox
- ES6+ JavaScript
- Clipboard API (for copy functionality)

## Disclaimer

This tool is for educational and artistic purposes. Use responsibly and in accordance with your repository host's terms of service.
