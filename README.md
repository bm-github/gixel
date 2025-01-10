# **Gixe, the Git Pixel Generator**

**Git Pixel Generator** is a fun and creative web-based tool that transforms your Git commit history into pixel-art-like patterns! Design custom contribution graphs to showcase your creativity directly on your GitHub profile.
Inspired by when GitHub changed the activity grid colours for Halloween.


---

## **Features**
- 🎨 **Interactive Grid**: Design directly on a grid that mimics GitHub's contribution graph.
- 🔥 **5-Intensity Levels**: Cycle through commit levels, from no commits (grey) to the darkest green.
- 📅 **Date-Aware Grid**: Automatically adjusts for different years, taking into account start and end days.
- 🛠️ **Script Generation**: Automatically creates a bash script to generate your commit patterns.
- 📂 **Download or Copy**: Easily download or copy the script for immediate use.
- 🎉 **Fully Customisable**: Works for any year you choose.

---

## **How It Works**

1. **Open the Tool**: Launch `gixel.html` in your browser.
2. **Design Your Pattern**:
   - Choose a year using the input field.
   - Click cells on the grid to set commit intensity:
     -  **Level 0 (Grey)**: No commits
     -  **Level 1 (Light Green)**: 1 commit
     -  **Level 2 (Medium Green)**: 2 commits
     -  **Level 3 (Dark Green)**: 3 commits
     -  **Level 4 (Darkest Green)**: 4+ commits
3. **Generate the Script**:
   - Click **"Generate Script"** to create a bash script.
   - Choose **"Copy to Clipboard"** or **"Download Script"** to save it.
4. **Run the Script**:
   - Make the script executable:
     ```bash
     chmod +x gixel-commits.sh
     ```
   - Run it in a Git repository:
     ```bash
     ./gixel-commits.sh
     ```
5. **Admire Your Art**: Push the changes to see your contribution graph transform into art!

   To start over, delete the repository and push a new script.
   Changes may take 24 hours
   To remove just delete the pixel repository


---

## **Example**

![example](/example.png)

---

## **Why Use Git Pixel Generator?**
- Express your creativity on GitHub.
- Make your profile stand out with unique art.
- It's easy to use and works seamlessly for any year!

---

## **Technical Details**
- **Empty Commits**: Uses `git commit --allow-empty` for clean commits.
- **Precise Timestamps**: Random times between 9:00 AM and 8:59 PM ensure natural-looking contributions.
- **Script Details**: Automatically pushes changes to the `main` branch for instant updates.

---

## **Styling**
- **GitHub-Inspired Design**:
  - Dark theme (`#0d1117`)
  - GitHub-style fonts and colours
- **Responsive Layout**: Works across devices with smooth hover effects.

---

## **Browser Compatibility**
The tool supports modern web features and works on all major browsers:
- **CSS Grid & Flexbox** for layout.
- **ES6+ JavaScript** for interactivity.
- **Clipboard API** for copying scripts.

---

## **Disclaimer**
This tool is for **educational and artistic purposes only**. Ensure your usage complies with GitHub's Terms of Service and repository guidelines.

---

## **Get Started**
1. Clone the repository: 
   ```bash
   git clone https://github.com/your-username/git-pattern-generator.git

## Feedback and Contributions

Have ideas for new features or improvements? Submit an issue or a pull request on GitHub!


## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this software under the terms of the license.