# tint2

tint2 is a simple, lightweight panel and taskbar designed for modern X window managers.

This repository is a **fork** of the original `tint2` project. Since the upstream development has ceased, this fork is aimed at actively maintaining the project, patching existing issues, and resolving future compatibility or bug problems.

*   **Latest stable release (upstream):** 17.0.2
*   **Upstream Changelog:** [ChangeLog](https://github.com/luanfagu/tint2/blob/master/ChangeLog)
*   **Documentation:** [doc/tint2.md](doc/tint2.md)

---

## What is tint2?

tint2 is a simple panel/taskbar made for modern X window managers. It was specifically designed for Openbox, but it integrates perfectly with other window managers (such as GNOME, KDE, XFCE, i3, etc.). It is based on `ttm`.

### Features

*   **Customizable Panel:** Configurable taskbar, system tray, clock, and launcher icons.
*   **Styling & Design:** Fully customize colors, transparency, borders, fonts, backgrounds, and gradients.
*   **Pager/Workspace Support:** Easily move tasks between workspaces (virtual desktops) and switch workspaces.
*   **Multi-Monitor Support:** Create separate panels per monitor displaying only the tasks corresponding to that monitor.
*   **Interactive Mouse Events:** Define custom mouse actions for clicking, scrolling, and dragging tasks.

### Core Goals

*   **Lightweight & Performant:** Keep memory and CPU usage as low as possible while maintaining a clean aesthetic.
*   **Standards Compliant:** Follow freedesktop.org specifications.
*   **Seamless Usability:** Provide a natural workflow for multi-desktop and multi-monitor setups.

---

## Build and Installation

### Prerequisites

Make sure to install the required [dependencies](https://github.com/luanfagu/tint2/wiki/Install#dependencies) for your distribution.

### Compilation

To compile `tint2` from source, run:

```bash
git clone https://github.com/luanfagu/tint2.git
cd tint2
mkdir build && cd build
cmake ..
make -j$(nproc)
```

### Installation

To install, run the following command as root (or via `sudo`):

```bash
make install
```

After installing, update your system's icon and MIME databases depending on your distribution:

**On Arch-based distros:**
```bash
gtk-update-icon-cache -q -t -f /usr/share/icons/hicolor
```

**On Ubuntu/Debian-based distros:**
```bash
update-icon-caches /usr/local/share/icons/hicolor && update-mime-database /usr/local/share/mime
```

Once installed, you can start the panel using `tint2` and configure it using the visual settings manager `tint2conf`.

---

## Troubleshooting & Known Issues

*   **Intel Graphics Glitches:** Graphical glitches on Intel graphics cards can be avoided by changing the acceleration method to UXA ([issue 595](https://github.com/luanfagu/tint2/issues/595)).
*   **Window Manager Compatibility:** Window managers that do not strictly adhere to the EWMH specification might experience minor interaction issues with tint2 ([issue 627](https://github.com/luanfagu/tint2/issues/627)).
*   **Transparency:** Full transparency requires a compositor such as Compton/Picom (unless your window manager has a built-in compositor, like Compiz, KWin, or Xfwm4).

---

## Contributing and Feedback

Please report any bugs, issues, or pull requests directly to the [GitHub Issue Tracker](https://github.com/luanfagu/tint2/issues). Your feedback and contributions are highly appreciated!

If you want to contribute, please check out the contribution guide: [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Useful Links

*   **GitHub Repository & Home:** [luanfagu/tint2](https://github.com/luanfagu/tint2)
*   **Documentation & Wiki:** [Tint2 Wiki](https://github.com/luanfagu/tint2/wiki/Home)
*   **Screenshots:** [Wiki Screenshots](https://github.com/luanfagu/tint2/wiki/screenshots)
*   **Demos:**
    *   [Compact panel, separator, and color gradients](https://github.com/luanfagu/tint2/wiki/whats-new-0.13.0.gif)
    *   [Executor plugin demo](https://github.com/luanfagu/tint2/wiki/whats-new-0.12.4.gif)
    *   [Mouse hover effects](https://github.com/luanfagu/tint2/wiki/whats-new-0.12.3.gif)
    *   [Workspace taskbar distribution](https://github.com/luanfagu/tint2/wiki/whats-new-0.12.gif)
*   **Historical Archive:** [tint2-archive on GitHub](https://github.com/luanfagu/tint2-archive/tree/master) or the [original Google Code downloads page](https://code.google.com/p/tint2/downloads/list)
