# 100Hires Portfolio Project – Setup

## Overview

This repository documents the setup process I completed for the first stage of the 100Hires hiring process. Since I had not used Cursor before, I treated this as a learning experience and documented each step along the way.

---

## Tools Installed

- Cursor IDE
- GitHub
- Git
- Claude Code Extension
- Codex Extension

---

## Setup Process

### 1. Installing Cursor

I downloaded and installed Cursor IDE from the official website. After installation, I signed in using my GitHub account.

### 2. Connecting GitHub

Cursor prompted me to connect my GitHub account. I authorized the connection and gave Cursor access to my repositories. I also selected my newly created repository (`100hires-project-setup`) during the setup process.

### 3. Installing Extensions

I installed the required extensions:
- Claude Code
- Codex

I signed into the extensions wherever authentication was required.

### 4. Creating the GitHub Repository

I created a public GitHub repository named `100hires-project-setup` for this project.

### 5. Learning the Cursor Interface

Since I was new to Cursor, I initially spent some time understanding the interface. At first, I was on the Agent screen instead of the actual editor, which confused me because keyboard shortcuts like `Ctrl + Shift + P` were opening the AI chat instead of the command palette.

After exploring the interface, I opened the Editor window and became familiar with how Cursor is organized.

### 6. Cloning the Repository

Initially, I tried using **Open Project**, assuming it would automatically open my GitHub repository. I later realized that the repository first needed to be cloned onto my computer.

After connecting GitHub successfully, Cursor displayed all of my repositories. I selected `100hires-project-setup`, chose a local folder, and cloned the repository successfully.

### 7. Creating the README

My repository was created without a README file, so I created a new `README.md` file manually inside the cloned repository and documented the entire setup process.

---

## Challenges I Faced & My Approaches

While finishing up the tool configurations and preparing to push my final updates, I encountered four real-world technical and configuration roadblocks. Here is exactly what went wrong and how I successfully troubleshooted them:

### 1. Git Configuration Pager Loop
While running basic environment configuration checks in the integrated terminal, PowerShell suddenly trapped me inside an interactive text stream showing lines marked with `...skipping...`. The terminal froze up and refused to accept any new commands.
- **How I solved it:** I recognized that Git was routing the text stream through the default system pager utility (`less`). I bypassed the loop instantly by pressing `q` on my keyboard to close the pager window and restore the active terminal prompt.

### 2. Windows Credential Manager Push Rejection
When I attempted to execute my initial code push (`git push`), Git threw an authentication failure warning stating `Invalid username or token`. It continuously rejected my authorization despite my login details being entirely accurate.
- **How I solved it:** I diagnosed that the Windows Credential Manager on my PC was holding onto an outdated, expired GitHub token from a past coding session, which was overriding my new login requests. 
  1. Opened **Windows Credential Manager** via the Control Panel.
  2. Located the broken entry under **Generic Credentials** for `git:https://github.com`.
  3. Removed the stale credentials completely.
  4. Executed `git push` again, which smoothly prompted the standard browser-based GitHub authorization flow and completed the push.

### 3. Claude Code Credit Balance Limit
After installing the Claude Code extension, I initiated the login flow. The browser redirect successfully authenticated my Anthropic account but then displayed a prompt to purchase commercial Console API usage credits or sign up for a premium plan. Back in Cursor, the extension interface successfully updated past the login window to show a live text input box stating *"Ask Claude to edit..."*. 
- **How I solved it:** To confirm whether the extension was fully active on the free tier, I ran a direct functional check by submitting a test message (`hello, are u working`). The extension processed the request but returned a server-side warning: `Credit balance is too low`. I successfully documented this structural monetization limit as part of my tool assessment.

### 4. Codex Operating System Incompatibility
When trying to run terminal commands to verify the secondary Codex extension framework, PowerShell generated a standard missing program alert (`CommandNotFoundException`).
- **How I solved it:** I reviewed the extension’s documentation on the marketplace dashboard and noticed it explicitly states: **`(MacOS only) Work with the ChatGPT macOS app`**. Because my local system runs on Windows, the command line interface cannot execute it natively. I documented this OS-level environment boundary accordingly.

---

## Verification Screenshots

I have mapped out the visual records of my configuration process, workspace tracking updates, and extension tests below:

### A. Git Tracking & Synchronization
- **Reference File:**
<img width="1920" height="1080" alt="Screenshot (383)" src="https://github.com/user-attachments/assets/c4178a71-8f78-49e2-98e2-ba63a4b7e372" />
 
  *(Displays successful terminal branch tracking updates, clean working trees, and successful repository push indicators)*

### B. Marketplace Extension Installations
- **Reference File:**
<img width="1920" height="1080" alt="Screenshot (384)" src="https://github.com/user-attachments/assets/b249b68e-c9cc-439a-a8d8-394b6a343db5" />
<img width="1920" height="1080" alt="Screenshot (385)" src="https://github.com/user-attachments/assets/161717ba-48c4-485c-aad4-6f8733b60b8b" />

  *(Confirms successful deployment of Anthropic's Claude Code extension directly inside the Cursor workspace IDE)*

### C. Authentication Handshake Flows
- **Reference Files:** 
<img width="1920" height="1080" alt="Screenshot (389)" src="https://github.com/user-attachments/assets/8f6e42c7-2a34-4799-b227-889cb52ee718" />

 *(The extension integration options panel in Cursor)*
 
<img width="1920" height="1080" alt="Screenshot (386)" src="https://github.com/user-attachments/assets/1a368772-235e-4f43-bb4b-72582f15d814" />

 *(The browser-side subscription requirement alert)*
 
<img width="1920" height="1080" alt="Screenshot (387)" src="https://github.com/user-attachments/assets/b898f444-9736-4683-b167-f12a850a88bc" />

 *(The Anthropic Console billing setup interface)*

### D. Claude Code Live Functional Testing
- **Reference Files:** 
<img width="1920" height="1080" alt="Screenshot (388)" src="https://github.com/user-attachments/assets/058fcbd6-da5a-4401-a7ff-6238e3a83a0f" />

 *(The unlocked input interface container prompting "Ask Claude to edit...")*
<img width="1920" height="1080" alt="Screenshot (390)" src="https://github.com/user-attachments/assets/20223fa0-14f0-4a7f-93e4-4448ecb1e303" />

 *(The active tool test showing the final server-side "Credit balance is too low" error catch)*

### E. Codex OS Environment Parameters
- **Reference File:**
<img width="1920" height="1080" alt="Screenshot (392)" src="https://github.com/user-attachments/assets/6e46f83b-b150-4c88-9458-ef6d71b93fa8" />
 
  *(The extension summary verifying the explicit macOS system restriction)*

---

## What I Learned

Completing this setup helped me become familiar with:

- Using Cursor IDE and navigating its custom workspace windows
- Connecting GitHub with Cursor and managing secure authentication pipelines
- Tracking down and deleting outdated system-cached keys via Windows Credential Manager
- Reading documentation carefully to identify OS-specific compatibility limitations (macOS vs. Windows)
- Intercepting terminal pager traps (`less`) and logging detailed API server errors
- Creating and maintaining structured documentation using Markdown to clearly track technical hurdles independently

---
*Harini DJ*
*Documentation updated on June 27, 2026.*
