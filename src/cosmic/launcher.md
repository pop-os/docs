# Launcher

The Launcher provides an overlay for opening new apps, switching between open apps, and performing other quick tasks. By default, it opens when the `Super` key is pressed.

![Launcher]()

The backend for the Launcher is provided by the [pop-launcher package](https://github.com/pop-os/launcher), which installs an IPC service. In the COSMIC Epoch desktop environment, the frontend is provided by the [cosmic-launcher package](https://github.com/pop-os/cosmic-launcher). (In older versions of Pop!_OS with GNOME, the frontend was provided by the [pop-shell package](https://github.com/pop-os/shell), which installs a GNOME extension.)

## Launching Apps

The Launcher allows searching through and launching any apps installed on the system. To launch an application, select it in the search results using the arrow keys and press `Enter`, or press `Ctrl` + the number of the search result.

![App launch]()

### Where Search Results Come From

Any `.desktop` file in a standard XDG data directory shows up as an application search result. The [freedesktop-desktop-entry](https://github.com/pop-os/freedesktop-desktop-entry) Rust crate is used to locate and parse the `.desktop` files.

The XDG data directories configured on your system can be viewed with the terminal command `echo $XDG_DATA_DIRS`. Common locations that search results come from include:

- `/usr/share/applications/` - System-wide .deb applications.
- `~/.local/share/applications/` - User account-specific `.desktop` files.
- `~/.local/share/flatpak/exports/share/applications/` - User-mode Flatpak packages.
- `/var/lib/flatpak/exports/share/applications/` - System-wide Flatpak packages.
- `/var/lib/snapd/...` - System-wide Snap applications.
- `/nix/var/nix/profiles/default` - System-wide Nix packages.
- `/nix/store` - System-wide Nix packages.
- `/nix/var/nix/profiles/per-user` - Per-user Nix packages.
- `~/.nix/...` - Per-user Nix packages.

## Switching Windows

## Performing Calculations

The Launcher has a built-in calculator that accepts [Qalculate!](https://qalculate.github.io/) expressions. To perform a calculation, use the prefix `=` followed by the expression.

Search queries starting with a numeric digit will also return calculator results automatically (sorted below open windows, but above installed applications).

## Searching the Web

The Launcher's built-in [web search plugin](https://github.com/pop-os/launcher/tree/master/plugins/src/web) allows quickly searching a number of websites and services. Below is a list of prefixes (in alphabetical order) which can be used to search the web.

<details>
<summary>Full list of prefixes (click to expand):</summary>

- `ali`, `alie`: AliExpress
- `amazon`: Amazon
- `arch`: Arch Wiki
- `bc`, `bandcamp`: Bandcamp
- `bing`: Bing
- `bs`, `brave`: Brave Search
- `crates`: Crates.io & Lib.rs
- `ddg`: DuckDuckGo
- `dev`: DEV Community
- `docs`: Docs.rs
- `eco`, `ecosia`: Ecosia Search
- `fedex`: Fedex
- `fh`, `flathub`: Flathub
- `gh`, `github`: GitHub
- `gist`: GitHub Gist
- `gs`, `google`: Google Search
- `gi`: Google Images
- `gm`: Google Maps
- `gn`: Google News
- `gsc`, `scholar`: Google Scholar
- `lib`: Libraries.io
- `mdn`: Mozilla Developer Network
- `npm`: NPM
- `pp`: Pop!_Planet
- `ppw`: Pop!_Planet Wiki
- `rdt`, `reddit`: Reddit
- `sc`, `sdcl`: Soundcloud
- `stack`: Stack Overflow
- `sp`, `startpage`: Startpage
- `twitch`: Twitch
- `ups`: UPS
- `wiki`: Wikipedia
- `www`: Opens any website with `https://` prefixed.
- `xaut`, `arxauth`, `arxivauthor`: ArXiv (by author)
- `xtit`, `arxtit`, `arxivtitle`: ArXiv (by title)
- `xabs`, `arxabs`, `arxivabstract`: ArXiv (by abstract)
- `xnum`, `arxnum`, `arxivnumber`: ArXiv (by ID number)
- `yh`, `yahoo`: Yahoo!
- `yt`, `youtube`: YouTube
</details>

When any of these prefixes are typed, the appropriate favicon is automatically downloaded directly from the service and saved to `~/.cache/pop-launcher/` to be displayed in the Launcher. However, the search query **is not sent** until you select the corresponding Launcher result to actually perform the search in a web browser.

## Running Commands

You can run terminal commands straight from the Launcher.

- To run a command interactively (in your default terminal), use the prefix `t:` followed by the command.
- To run a command non-interactively (in the background, with no visual feedback), use the prefix `:` followed by the command.

---

# App Library

If you prefer to browse through all of your installed applications, or you want to search only your installed applications (without searching open windows and other sources), you can alternatively use the App Library. To open the App Library, press `Super` + `A` or click `Applications` in the top right of the screen.

The App Library displays icons defined in `.desktop` files, using the same [sources](#where-search-results-come-from) as the Launcher.

## Searching

To search within the App Library, just start typing while it's open. Applications that are available to install in the Pop!_Shop will show up below your installed applications in the search results.

![App Library Search]()

## Sorting Apps

You can create new folders or switch between existing folders using the buttons at the bottom of the App Library.

![App Library Folders]()

To move an app to a different folder, drag and drop its icon over that folder.