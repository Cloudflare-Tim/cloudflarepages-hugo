# Readme Template

This repository contains a Hugo-based documentation site template that's ready to deploy to Cloudflare Pages.

visit this example here https://timsnotes.pages.dev/

## Quick Start

1. Fork this repository:

2. Deploy to Cloudflare Pages:
   - Go to Cloudflare Pages
   - Click "Create application"
   - Choose "Pages"
   - Select your cloned repository that you just made
   - Use these build settings:
     - Framework Present: `Hugo`
     - Build command: `hugo`
     - Build directory: `public`
     - Environment variable: `HUGO_VERSION` : `0.139.3`
     - Environment variable: `HUGO_ENV` : `production`

That's it! Your site will be live at `[your-project].pages.dev`

## Site Structure

```
content/
├── _index.md          # Main landing page
├── topic1/           
│   ├── _index.md     # Topic overview
│   ├── subtopic1/    
│   │   └── _index.md # Subtopic content
│   └── subtopic2/
│       └── _index.md
└── [other topics]
```

## Creating Content

### File Format
Every markdown file should start with frontmatter:

```md
---
title: "Your Page Title"
description: "Brief description"
date: 2024-12-11
draft: false
---
```
* if draft: true is set, it will not publish publicly


### Markdown Examples

#### Basic Formatting
```md
# Heading 1
## Heading 2
### Heading 3

**Bold text**
*Italic text*
~~Strikethrough~~

> This is a blockquote
```

#### Lists
```md
- Bullet point
- Another point
  - Nested point
  - Another nested point

1. Numbered list
2. Second item
   1. Nested numbered item
   2. Another nested item
```

#### Code
````md
```python
def hello_world():
    print("Hello, World!")
```
````

#### Links
```md
# Internal Links
- [Link to Topic 1](/topic1)
- [Link to Subtopic](../subtopic1)
- [Relative link to sibling page](./another-page)

# External Links
[OpenAI](https://openai.com)
```

#### Images
```md
![Alt text](/images/example.png)
```

#### Tables
```md
| Header 1 | Header 2 |
|----------|----------|
| Cell 1   | Cell 2   |
| Cell 3   | Cell 4   |
```

### Link Structure Examples

1. From a topic page to its subtopics:
```md
- [Subtopic 1](subtopic1)
- [Subtopic 2](subtopic2)
```

2. From a subtopic back to its parent:
```md
[Back to Topic 1](..)
```

3. From any page to the home page:
```md
[Home](/)
```

4. Between sibling subtopics:
```md
[Next Subtopic](../subtopic2)
```

## Customization

### Site Configuration
Edit `hugo.toml` to change:
- Site title
- Base URL (currently using relative path)
- Language settings
- Theme options

### Adding New Topics
1. Create a new directory in `content/`
2. Add an `_index.md` file
3. Add your content files
4. Push to GitHub - Cloudflare will automatically deploy changes

## Custom Hostname
This build uses relative path so custom hostname does work

## Troubleshooting

### Common Issues
1. Build fails: Check HUGO_VERSION in Cloudflare Pages settings
2. Missing content: Ensure frontmatter is properly formatted
3. Broken links: Check relative path structure

Need help? Open an issue on GitHub!
