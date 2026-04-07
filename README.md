# FFoxxy

A custom Firefox theme.

---

## Requirements

- Mozilla Firefox (tested on current stable)
- `toolkit.legacyUserProfileCustomizations.stylesheets` enabled in `about:config` (see below)

---

## Installation

### 1. Clone or download the repository

```bash
git clone https://github.com/Inggo/FFoxxy.git
```

### 2. Install the XPI theme

Open Firefox and navigate to:

```
about:addons
```

Click the gear icon ⚙️ → **Install Add-on From File...**, then select `ffoxxy-theme.xpi` from the cloned repo.

Alternatively, you can drag and drop `ffoxxy-theme.xpi` directly into a Firefox window.

### 3. Enable userChrome.css support

Open `about:config` in Firefox and set the following preference to `true`:

```
toolkit.legacyUserProfileCustomizations.stylesheets
```

### 4. Locate your Firefox profile folder

Navigate to `about:support` in Firefox, then under **Application Basics**, click **Open Directory** next to **Profile Directory**.

This will open a folder like:

```
~/.mozilla/firefox/xxxxxxxx.default-release/
```

### 5. Link the chrome folder (recommended)

Instead of copying files, symlink the `chrome/` folder from the repo into your profile. This way your customizations stay in sync with the repo.

```bash
# Replace the path with your actual profile directory
ln -s /path/to/FFoxxy/chrome ~/.mozilla/firefox/xxxxxxxx.default-release/chrome
```

If a `chrome/` folder already exists in your profile directory, remove or back it up first:

```bash
rm -rf ~/.mozilla/firefox/xxxxxxxx.default-release/chrome
```

### 6. Restart Firefox

Close and reopen Firefox for the `userChrome.css` changes to take effect.

---

## Updating

Since the `chrome/` folder is symlinked, pulling the latest changes is all you need:

```bash
cd /path/to/FFoxxy
git pull
```

Then restart Firefox.

---

## License

[MIT](LICENSE)
