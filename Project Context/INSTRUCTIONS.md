## Authoring Instructions

These notes are for future updates and for assistants working on this repository.

### Goal
Keep every recipe page consistent and ensure the homepage always lists all available recipes.

### When creating or updating a recipe
1. Create or update `recipes/<slug>/index.html` using the universal recipe UI:
   - Cook Mode toggle
   - Step checklists with Prev/Next navigation
   - Optional timers per step (when the recipe benefits from them)
   - Keep Screen Awake button (Wake Lock when supported)
   - Home navigation button in the header actions:
     ```html
     <a href="/" class="btn" aria-label="Home">Home</a>
     ```
2. Update the homepage links in `index.html`:
   - Append a new list item inside the main `<ul>` with this pattern (adjust title and tags as needed):
     ```html
     <li><a href="recipes/<slug>/" title="Recipe Title">Recipe Title <span class="tag">cook mode</span></a></li>
     ```
   - Keep the existing indentation and formatting style.
3. Keep file paths and naming consistent:
   - Directory: `recipes/<slug>/`
   - Entry point: `index.html`
4. Verify locally by opening the new recipe and the homepage in a browser.

### Commit and deploy
- Commit all changes with a descriptive message and push to `main`:
  - Example: `git add . && git commit -m "Add <recipe title> and update homepage" && git push`
- Netlify deploys automatically from GitHub. No build step is required. The publish directory is the repo root (`.`).

### Promise (assistant behavior)
Whenever asked to create a new recipe in this repository:
- Also add or update the corresponding link on the homepage (`index.html`) in the same change set.
- Preserve existing indentation and formatting in edited files.
- If a recipe already exists, ensure the homepage entry stays accurate.


