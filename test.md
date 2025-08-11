# Let's create the folder structure and markdown files with the provided content
import os

# Define base folder
base_folder = "/mnt/data/technical-writing-roadmap"

# Define structure
folders = [
    "",
    "resources"
]

files_content = {
    "README.md": """# Technical Writing Roadmap

Welcome to the **Technical Writing Roadmap** — a free, open-source guide for anyone looking to become a skilled technical writer.

Inspired by the *Gold-Star Drafts* program, this roadmap takes you from setting up your tools to landing your first freelance gig, with resources and exercises at each stage.

---

## 📚 Roadmap

1. [Introduction](00-introduction.md)
2. [Getting Started](01-getting-started.md)
3. [Grammar & Syntax](02-grammar-and-syntax.md)
4. [Content Creation](03-content-creation.md)
5. [SEO](04-seo.md)
6. [Job Market](05-job-market.md)
7. [Final Tips](06-final-tips.md)

---

## 💡 Who is this for?
- Beginners interested in technical writing
- Developers who want to share their knowledge
- Career changers looking to enter the writing space

---

## 🤝 Contributing
We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## 📜 License
This project is licensed under the [MIT License](LICENSE).
""",
    "00-introduction.md": """# Introduction

Welcome to the **Gold-Star Drafts: Technical Writing Roadmap**.

This guide will walk you step-by-step through the skills, tools, and mindset needed to become a successful technical writer.

---
""",
    "01-getting-started.md": """# Getting Started as a Writer

## 🛠 Tools & Accounts
- Professional email (e.g., yourname@gmail.com)
- Google Workspace/Docs
- Scheduling tools: Google Calendar, Calendly
- Publishing platforms: Medium, HashNode, or a personal site
- Portfolio: LinkedIn profile
- Microdomains: X (Twitter) for networking
- Developer tools: GitHub/GitLab + Markdown
- Communication tools: Slack, Discord
- Identity provider (Google/Microsoft) + password manager

> **Rule:** Excellent writing comes from great reading — garbage in, garbage out!
""",
    "02-grammar-and-syntax.md": """# Grammar & Syntax Refresher

Great writing stems from well-organized, clear thinking and a personal style.

---

## 🎯 Resources
- [Google Technical Writing Course](https://developers.google.com/tech-writing)
- [Best Technical Writing Books](https://technicalwriterhq.com/writing/technical-writing/technical-writing-books/)
- [Draft.dev Style Guide](https://draft.dev/learn/technical-writer-style-guides)
""",
    "03-content-creation.md": """# Content Creation

Types of technical content:
- Tutorials
- Guides
- Roundups
- Comparisons
- Thought leadership
- Persuasive content

> Start with the first four. Save the last two for when you have more experience.
""",
    "04-seo.md": """# SEO Basics

SEO (Search Engine Optimization) is essential for writing content that reaches people.

---

## 🔗 Resources
- [Beginner's Guide to SEO](https://neilpatel.com/what-is-seo/)
- [SEO Checklist](https://nealschaffer.com/seo-checklist/)
- [Long-tail Keywords](https://yoast.com/focus-on-long-tail-keywords/)
""",
    "05-job-market.md": """# Entering the Job Market

Your online presence is your portfolio.

## 🌐 Platforms
- LinkedIn (polished profile)
- Twitter/X (engage with communities)
- Job boards (see resources/job-boards.md)
""",
    "06-final-tips.md": """# Final Tips

- Write a lot — improvement comes with practice
- Keep reading and learning
- Build your network
- Be consistent with your style guide
- Keep your portfolio updated
""",
    "resources/links.md": """# Useful Links

A collection of all resources mentioned in the roadmap, organized by category.
""",
    "resources/style-guides.md": """# Style Guides

- [Google Technical Writing Course](https://developers.google.com/tech-writing)
- [Draft.dev Style Guide](https://draft.dev/learn/technical-writer-style-guides)
""",
    "resources/seo-resources.md": """# SEO Resources

- [Beginner's Guide to SEO](https://neilpatel.com/what-is-seo/)
- [SEO Checklist](https://nealschaffer.com/seo-checklist/)
- [Long-tail Keywords](https://yoast.com/focus-on-long-tail-keywords/)
""",
    "resources/job-boards.md": """# Job Boards

- [BestWriting](https://bestwriting.com/jobs)
- [CryptoJobs](https://crypto.jobs/)
- [Who Pays Writers](http://whopayswriters.com/)
"""
}

# Create folders
for folder in folders:
    os.makedirs(os.path.join(base_folder, folder), exist_ok=True)

# Write files
for path, content in files_content.items():
    with open(os.path.join(base_folder, path), "w", encoding="utf-8") as f:
        f.write(content)

base_folder
