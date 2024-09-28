---
layout: post
title: "roam-css-tweaks"
date: 2024-09-28
author: Everett Liu
---

## scrollbar

Tip: Scrollbars Plugin 无法为 Roam Portal / All Pages 创建滚动条，而这段 snippet 是可以的。 

```css
/* scrollbar */
::-webkit-scrollbar {
    width: 15px;
    background-color: rgba(196, 181, 253, 0.3); /* rgba(15,118,110,0.2), rgba(234,64,126,0.2) */
}
```

## Roam Color Highlighter

my self-defined data-tags:

```css
/* Set highlight */
[data-tag="c:indigo"] + .rm-highlight {
  background-color: #6366f1 !important;
  color: white !important;
}
[data-tag="c:dark-blue-1"] + .rm-highlight {
  background-color: #2B7396  !important;
  color: white !important;
}
[data-tag="c:purple"] + .rm-highlight {
  background-color: #a855f7 !important;
  color: white !important;
}
[data-tag="c:dark-red-1"] + .rm-highlight {
  background-color: #BF1828 !important;
  color: white !important; 
}
[data-tag="c:rose"] + .rm-highlight {
  background-color: #fb7185 !important;
  color: white !important; 
}
[data-tag="c:pink"] + .rm-highlight {
  background-color: #f472b6 !important;
  color: white !important; 
}
[data-tag="c:light-pink-rose"] + .rm-highlight {
  background-color: #FFB5CF !important;
  color: black !important; 
}
[data-tag="c:emerald"] + .rm-highlight {
  background-color: #6ee7b7 !important;
  /* color: white !important; */
}
[data-tag="c:lime"] + .rm-highlight {
  background-color: #bef264 !important;
}
[data-tag="c:lavendar"] + .rm-highlight {
  background-color: #E9E9FA !important;
}
[data-tag="c:MistyRose"] + .rm-highlight {
  background-color: #FFEEED !important;
}
[data-tag="c:SpringGreen"] + .rm-highlight {
  background-color: #BFFFDF !important;
}
[data-tag="c:amber"] + .rm-highlight {
  background-color: #fcd34d !important;
  color: white !important; 
}
[data-tag="c:light-orange-1"] + .rm-highlight {
  background-color: #FFC8A7 !important;
  color: black !important; 
}

/* Set text */
[data-tag="c:indigo"] + .rm-bold {
  color: #312e81 !important;
  font-weight: bold;
}
[data-tag="c:dark-blue-1"] + .rm-bold {
  color: #1C4C63   !important;
  font-weight: bold;
}
[data-tag="c:purple"] + .rm-bold {
  color: #581c87 !important;
  font-weight: bold;
}
[data-tag="c:dark-red-1"] + .rm-bold {
  color: #BF1828 !important;
  font-weight: bold; 
}
[data-tag="c:rose"] + .rm-bold {
  color: #9f1239 !important;
  font-weight: bold; 
}
[data-tag="c:pink"] + .rm-bold {
  color: #be185d !important;
  font-weight: bold;
}
[data-tag="c:light-pink-rose"] + .rm-bold {
  color: #FFB5CF !important;
  font-weight: bold;
}
[data-tag="c:emerald"] + .rm-bold {
  color: #047857 !important;
  font-weight: bold;
}
[data-tag="c:lime"] + .rm-bold {
  color: #65a30d !important;
  /* font-weight: bold; */
}
[data-tag="c:lavendar"] + .rm-bold {
  color: #B9B9C7 !important;
  font-weight: bold;
}
[data-tag="c:MistyRose"] + .rm-bold {
  color: #E6D6D5 !important;
  font-weight: bold;
}
[data-tag="c:SpringGreen"] + .rm-bold {
  color: #A8E0C4 !important;
  font-weight: bold;
}
[data-tag="c:amber"] + .rm-bold {
  color: #d97706 !important;
}
[data-tag="c:light-orange-1"] + .rm-bold {
  color: #FFC8A7 !important;
}

/* Set underline */
[data-tag="c:indigo"] + em {
  border-bottom: 3px solid #4f46e5;
}
[data-tag="c:dark-blue-1"] + em {
  border-bottom: 3px solid #286E8F;
}
[data-tag="c:purple"] + em {
  border-bottom: 3px solid #7e22ce;
}
[data-tag="c:dark-red-1"] + em {
  border-bottom: 3px solid #BF1828;
}
[data-tag="c:rose"] + em {
  border-bottom: 3px solid #e11d48;
}
[data-tag="c:pink"] + em {
  border-bottom: 3px solid #ec4899;
}
[data-tag="c:light-pink-rose"] + em {
  border-bottom: 4px solid #FFB5CF;
}
[data-tag="c:emerald"] + em {
  border-bottom: 3px solid #10b981;
}
[data-tag="c:lime"] + em {
  border-bottom: 3px solid #84cc16;
}
[data-tag="c:lavendar"] + em {
  border-bottom: 5px solid #E2E2F2;
}
[data-tag="c:MistyRose"] + em {
  border-bottom: 5px solid #F5E4E4;
}
[data-tag="c:SpringGreen"] + em {
  border-bottom: 5px solid #B4F0D2;
}
[data-tag="c:amber"] + em {
  border-bottom: 3px solid #fbbf24;
}
[data-tag="c:light-orange-1"] + em {
  border-bottom: 3px solid #FFC8A7;
}
```

## Roam Studio

my customization:

```css
:root {
    --bc-main: rgba(252, 231, 243, 0.5); /* for dark: rgba(51, 65, 85, 0.7) */
    --bc-right-sidebar__content: rgba(253, 164, 175, 0.2); /* for dark: rgba(107, 114, 128, 0.8), var(--cl-coolGray-500) */

    /* --co-main: var(--cl-cyan-900); /* --co-main: var(--cl-warmGray-200); cl-gray-400; 考虑一下深棕色？ */
	/* --ff-main: 'iA Writer Quattro S'; /* iA Writer Quattro S, iA Writer Mono S, segoe ui, Bookerly, Bebas Neue */
	--fs-main: 16px; /* --fs-main: 1.1rem; */
	--fw-main: normal;
  
	--bc-main__inline-code: var(--cl-indigo-100); /* --cl-gray-600 */
	--bt-main__inline-code: transparent;
	--br-main__inline-code: transparent;
	--bb-main__inline-code: transparent;
	--bl-main__inline-code: transparent;
	--bd-main__inline-code: 3px;
	--co-main__inline-code: var(--cl-pink-600); /* var(--cl-lime-300) */
	/* --ff-main__inline-code: 'iA Writer Duo S'; /* iA Writer Duo S, Georgia */
	--fs-main__inline-code: 17px; /* --fs-main__inline-code: 1.2rem; */

    --bc-topbar: rgba(245, 208, 254, 0.3); /* rgba(19, 78, 74, 0.3) */
	--bb-topbar: 1px solid var(--cl-black);

    --bc-right-sidebar__toprow: rgba(249, 115, 22, 0.3); /* rgba(54, 83, 20, 0.6), var(--cl-lime-900) */
	--bb-right-sidebar__toprow: 1px solid var(--cl-black);
    --bb-right-sidebar__window: 1px solid var(--cl-black);
	--fs-right-sidebar__window: 1rem;
    --co-right-sidebar__window-headers: var(--cl-gray-600);
    --co-right-sidebar__h1: var(--cl-fuchsia-700); /* var(--cl-fuchsia-200) */
	--fs-right-sidebar__h1: 1.3rem;
	--fw-right-sidebar__h1: 700;
}
```

## font

```css
@import url('https://cdn.staticfile.org/lxgw-wenkai-screen-webfont/1.6.0/lxgwwenkaiscreen.css');

* {
  /* Screen version */
  font-family: "Inter", "LXGW WenKai Screen", sans-serif;
}
```
