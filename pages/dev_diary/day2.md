---
title: Day 2
date: 2022/03/05
description: Transforming to tsx and creating diaries.
tag: web development
author: You
---

I started to work on transforming js. files to .tsx. I did happen to encounter some difficulties in removing the Ts errors:

## Problems 
1. I Wasn't sure if I should replace "require" with ES6 import in files for node.js execution(Solved)
2. I had a problem with annotating one function(Solved)
3. I had a problem with finding a way to properly import modules "path" and "fs" for .tsx(Solved)

## Solutions
1. TypeScript will transpile ES6 code to appropriate code in node.js.
2. In this case, I trusted in .tsx quick fix. But in this case, it wasn't a proper fix. I removed the annotation as I repaired the last bug
3. I did get the error information in my VsCode, and I was searching the internet for a fix. I thought that importing "@type/path" or "@types/fs" will make it work. In the end, I came up with a solution, "npm install typescript". It still didn't work, and the error remained. After a while, I come up with a fix. I installed something which could import the working of the VsCode. So I restarted it.

Later I started to work on Dev diaries and Markdown files. Then created the section and the first two posts. Quite easy copy-pasting the template section. 
