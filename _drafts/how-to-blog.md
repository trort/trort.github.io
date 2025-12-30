---
layout: post
title:  "Comprehensive Guide to Blogging"
---

# How to Write Blogs

This is a comprehensive guide to writing, formatting, and publishing posts on your Jekyll blog.

## 1. The Workflow: From Draft to Published

### Step 1: Start a Draft
1.  Create a new file in the `_drafts` folder.
2.  Name it `your-topic.md` (no date needed yet).
3.  Add the **Front Matter** at the top (see Section 2).
4.  Write your content using Markdown.
5.  **Save and Push**: You can commit and push this file to GitHub. Since it is in `_drafts`, it will **not** be visible on the live site.

### Step 2: Publish
1.  Move the file from `_drafts` to the `_posts` directory.
2.  Rename the file to include the date: `YYYY-MM-DD-your-topic.md`.
    - Example: `2025-12-30-my-new-post.md`
3.  Update the `date` in the Front Matter to match.
4.  Commit and push to GitHub. The site will update automatically.

---

## 2. Front Matter
Every post must start with a "Front Matter" block enclosed by triple dashes (`---`). This tells Jekyll how to process the file.

```yaml
---
layout: post
title:  "Your Post Title Here"
date:   2025-12-30 12:00:00 -0500
categories: [updates, tech]
tags: [jekyll, guide]
---
```

*   **layout**: Always use `post`.
*   **title**: The title that appears on the site.
*   **date**: YYYY-MM-DD format.
*   **categories/tags**: specific keywords for organizing content.

---

## 3. Formatting Content (Markdown)

### Headers
Use `#` for headers.
```markdown
# H1 (Title size)
## H2 (Section)
### H3 (Subsection)
```

### Text Styles
*   **Bold**: `**text**` -> **text**
*   *Italic*: `*text*` -> *text*
*   [Link](https://google.com): `[Link](https://google.com)`

### Lists
**Bulleted:**
*   Item 1
*   Item 2

**Numbered:**
1.  First step
2.  Second step

### Code Blocks
Wrap code in triple backticks. Specify the language for syntax highlighting.

\`\`\`python
def hello():
    print("Hello world!")
\`\`\`

### Blockquotes
> This is a quote.
> It can span multiple lines.

---

## 4. Adding Images
1.  Create an `assets/images` folder in your repository if it doesn't exist.
2.  Upload your image there (e.g., `screenshot.png`).
3.  Link it in your post:
    `![Description of image](/assets/images/screenshot.png)`
