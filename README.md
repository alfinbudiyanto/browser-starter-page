# 🌌 Glossy Purple Sysadmin Dashboard

A lightweight, zero-data overhead, and privacy-focused browser start page designed for system administrators and developers. Built with pure vanilla HTML, CSS, and JavaScript, it features a modern glassmorphism aesthetic tailored for Fedora Linux users.

## 🚀 Key Features

- **Zero-Data Overhead:** Runs entirely locally on your hard drive. No internet connection or heavy external frameworks (Bootstrap, Tailwind, jQuery) are required to load the page.
- **Glassmorphism Aesthetic:** Premium "Glossy Purple" theme featuring modern translucent cards, blur backdrops, subtle radial gradients, and dynamic interactive hover glowing effects.
- **Dynamic Headers & Clock:** Displays real-time greetings based on the hour of the day (Morning, Afternoon, Evening, Night) alongside a precise live clock (`HH:MM:SS`).
- **Live Net Status:** Monitors system network state in real-time, instantly rendering an `ONLINE` (green) or `OFFLINE` (red) status indicator.
- **Persistent Scratchpad:** An integrated monospace text area for stacking frequently used DNF or Docker commands. It utilizes browser `localStorage` to ensure notes persist across browser sessions and OS reboots without backend servers.
- **One-Click Clipboard Utility:** Built-in dashboard shortcuts allowing the user to copy the entire scratchpad workspace instantly or safely wipe its data contents via confirmation flags.

---

## 🌿 Repository Workflow & Branches

This repository maintains two separate tracking environments to isolate configuration states:

1. **`main` (or production branch):** Stores the stable, pristine template code.
2. **`running` (active runtime branch):** The operational playground that serves as the actual live entry point for the browser.

### The `running` Branch Architecture

```text
╭─ alfinbudiyanto@this.fedora.fin
│  ~/.../starter_page (running|✔)
╰─❯ git desc running
its branch only for running in system then its will changing as what user do, its not commited except needed
```

- **Volatile Operations:** This branch lives directly on your local system to handle active runtime adjustments.
- **No-Commit Policy:** Modifications made here reflect user-specific runtime preferences (such as personal configurations or transient changes). They are **not committed or pushed** to upstream repositories unless an essential platform-wide architectural change is required.

---

## 🛠️ How to Use & Deploy

### 1. Cloning and Setting Up Environments

Clone the repository and verify your positioning on the active execution branch:

```bash
git clone <repository-url> starter_page
cd starter_page
git checkout running
```

### 2. Linking to Web Browser

Since the page runs at absolute warp speed via the local filesystem, link the runtime file directly to your browser's startup configurations:

1. Open your browser (e.g., Chromium, Firefox, Brave).
2. Press `Ctrl + O`, locate, and select the `homepage.html` file inside your project path.
3. Copy the entire file URL scheme from the address bar (it will output exactly as: `file:///home/alfinbudiyanto/.../starter_page/homepage.html`).
4. Access your browser's **Settings / Preferences**.
5. Navigate to **Home Page / New Tab** configurations, select **Custom URL**, and paste the copied `file:///` address into the payload slot.

Now, every time a new browser workflow is spawned, your ultra-lightweight dashboard will render instantly.
