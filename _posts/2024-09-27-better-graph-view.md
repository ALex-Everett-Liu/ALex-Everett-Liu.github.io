---
layout: post
title: "better-graph-view"
date: 2024-09-27
author: Everett Liu
---

basic GUI through tkinter:

```python
    root = tk.Tk()
    root.title("Graph Builder")
    root.geometry("500x400")  # Set window size root.geometry("500x350")

    style = {
        'font': ('Montserrat', 15),
        'width': 25,
        'height': 2,
        'bg': '#2B7396',
        'fg': 'lightgreen',
    }
```

set font to Montserrat: A more geometric and modern sans-serif font [that's trendy and eye-catching]. (recommended by ChatGPT: Arial looks not so good, can you recommend an alternative font for me?)
