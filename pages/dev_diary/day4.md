---
title: Day 4
date: 2022/03/17
description: Debugging deployment
tag: web development
author: You
---

Vercel console showed me some errors and my I application couldnt be deployed. I followed the instructions from debugging console in Vercel.

### Problems

1 && 2 && 3 Deployment is not working. Vercel console show errors.

### Solutions
1.  I removed yarn.lock, since yarn was installed at the begging. I prefer npm. There shouldn't be two package managers in deployed version.
2. I have changed the "gen-rss.js" from js to .tsx, and it was a problem.
    - I fixed the path and extension of the file in package.json from ".../gen-rss.js" to ".../gen-rss.tsx".
    - It imported the script correctly, but it had a problem " cannot use import statement outside of module".
    - I checked the imports on my Github and wanted to copy-paste them and fix the tsx.config.
    - I decided to keep this file as .js and reverted previous changes.
3. Another problem with .tsx appeared. 
    - I found a solution to be running "npm i --force", but it was blocked by git. I removed node modules directory and reinstalled everything.
    - It didn't had any impact, so I disabled SWC Ts/js compiling by adding .babelrc
    
That fixed the errors on Vercel and I deployed finally.

After having a deployable main branch, I did a rebase on both feature branches. Later I searched the internet for some inspiration for the design of the website.