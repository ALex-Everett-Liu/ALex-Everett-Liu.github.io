---
layout: post
title: "GitHub-Pages-setup-issues"
date: 2024-09-27
author: Everett Liu
---

# GitHub Pages 踩坑记录

1. 终于发现问题在于删掉了 `_config.yml` 中的 future 字段，日期那一栏填的 2024-09-28 就解析不出来了，因为当前的 UTC 时间 TM 的还是 2024-09-27！（咱们东八区比 UTC 快八个小时……）

2. encoding issue

Q (me): I finally find what's wrong:
When I edit index.html directly in Github repo this time, it shows that:
"We've detected the file encoding as UTF-16LE. When you commit changes we will transcode it to UTF-8."
So I just delete this index.html and re-create a new index.html with the same content, this time all things works well.
but, I just wonder why this happened? 

A (ChatGPT): When you edit a file directly in the GitHub repository, GitHub's web interface automatically detects the file encoding. If the file is not saved with the correct encoding, it can cause issues. In this case, the file was being saved as UTF-16LE, which is not compatible with the default UTF-8 encoding used by most systems.

When you deleted the file and created a new one with the same content, the new file was saved with the correct UTF-8 encoding, resolving the issue.

To summarize, the problem was due to the file being saved as UTF-16LE, which was causing issues when committed. Deleting the file and creating a new one with the same content resolved the issue by ensuring the file was saved with the correct UTF-8 encoding.

A (Claude): [Thank you for sharing what resolved the issue]. This is an interesting problem, [and it's great that you found the solution]. Let's dive into why this happened:
[This situation highlights the importance of] consistent [[file encoding]] in web development and version control. [It's a subtle issue that can cause unexpected problems], so it's good to be aware of it.

UTF-16LE vs UTF-8:
UTF-16LE (Little Endian) is a Unicode encoding that uses 2 or 4 bytes per character.
[[UTF-8]] is [a more common encoding] [for web content], using 1 to 4 bytes per character.

Why it happened:
This can occur if you [edited the file with a program that saved it in UTF-16LE format]. [Common culprits include] some Windows text editors or applications.
It might have happened if you [copied content from a source that was in UTF-16LE] and [pasted it directly into GitHub's web editor].

Why it caused problems:
Web servers and browsers [typically expect UTF-8 encoding for HTML files].
[While GitHub offered to transcode it to UTF-8 upon commit], [there might have been some issues in how this was processed or served].

Why recreating the file worked:
[By creating a new file directly in GitHub's web interface], you ensured it was in UTF-8 format from the start.

Best practices to avoid this:
Use text editors [that default to UTF-8 encoding].
When copying content, be aware of potential [encoding issues].
If editing locally, consider using a .gitattributes file to [enforce text file encoding].

For future reference:
If you encounter this again, [you can usually fix it by opening the file in a text editor] that supports different encodings, then saving it as UTF-8.