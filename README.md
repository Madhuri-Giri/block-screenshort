# Screenshot-Protection Web Page

This project is a demo page created as part of a frontend development task.  
The goal is to simulate screenshot protection using only HTML5, CSS3, and vanilla JavaScript, without using any external libraries, frameworks, or CDNs.

# Project Overview

This single-page demo displays sample confidential content including a heading, paragraphs, and placeholder images.  
The JavaScript logic detects screenshot-like actions and triggers UI masking such as blur effects and overlay warnings.

Due to browser/OS limitations, websites cannot fully block hardware-level screenshots.  
However, the page implements maximum possible web-based protection techniques to mimic screenshot blocking behavior.

# Features Implemented

# Prevents Browser Interactions

- Right-click disabled
- Text selection disabled
- Copy and paste blocked

# Developer Tools Blocking

- F12 blocked
- Ctrl + Shift + I blocked
- Ctrl + U blocked
- Ctrl + Shift + C & J blocked

# Screenshot Attempt Detection

- Detects PrintScreen key
- Clears clipboard on PrintScreen
- Shows blocking overlay
- Blurs page temporarily

# Mobile/Touch Defense

- Long-press disabled
- Multi-touch detection
- 3-finger touch triggers blur

# Visual Security

- Blur effect on tab switching
- Full-screen overlay message

# How Screenshot Blocking Works (HTML/CSS/JS Only)

Web browsers do not allow access to system-level screenshot events.  
So this project uses the following techniques:

# 1. Keyboard Event Monitoring

if (e.key === "PrintScreen") { showBlocker(); }

# 2. Clipboard Clearing

navigator.clipboard.writeText("");

# 3. Tab Visibility Detection

document.addEventListener("visibilitychange", ...)

# 4. Touch Event Detection

if (e.touches.length >= 3) { showBlocker(); }
