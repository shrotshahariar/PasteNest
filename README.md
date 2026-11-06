<p align="center"><img src="pastenest-icon.png" width="88" height="88" alt="PasteNest app icon"></p>

# PasteNest

A local clipboard history for macOS. Open the menu-bar picker, find something you copied, and click once to paste it back into the app you were using.

**[Download PasteNest 1.4 for Apple Silicon](https://github.com/shrotshahariar/PasteNest/releases/download/v1.4.0/PasteNest-1.4-macOS-arm64.zip)** · [Release notes and checksum](https://github.com/shrotshahariar/PasteNest/releases/tag/v1.4.0)

<p><img src="picker.png" width="600" alt="PasteNest's light quick-paste window showing sample clips and their source apps"></p>

## Getting started

1. On an Apple Silicon Mac running macOS 13 or later, download the ZIP, extract it, and move **PasteNest.app** to Applications.
2. Launch PasteNest and copy some text, a link, or an image.
3. Press **⌘⇧Space**. Search or use the arrow keys, then click a row or press Return. The picker opens on the display under your pointer.

For automatic insertion, allow the installed app under **System Settings → Privacy & Security → Accessibility**. Some macOS versions call this **Device Control and Data Access**. You can also use **Copy** and paste manually. This release is ad-hoc signed and has not been notarized by Apple. Gatekeeper may block the downloaded build.

## Get Info

Open a clip’s **…** menu or right-click it, then choose **Get Info**. Use **Preview** to read the clip and **Done** to return to the picker.

<p><img src="get-info.png" width="310" alt="The Get Info tab for a sample TextEdit clip, showing its source, last copy time, type, collection, and character count."></p>

## In the menu bar

The folded-paper icon shows when a clip reaches your history. A sheet slips into the pocket and turns into a brief checkmark. Pausing capture shows two steady bars. With macOS Reduce Motion enabled, successful copies show the checkmark immediately.

<details><summary>Preview the menu-bar icon in motion</summary>

<img src="menu-feedback.png" width="350" alt="The PasteNest icon and its monochrome menu-bar mark move from ready to saved, paused, and ready again.">

</details>

## Text filters

Open the **…** menu on a text or link clip and choose **Paste with Filter**. Extract Web Links and Extract Email Addresses paste each distinct match on a new line, in its original order. Markdown Blockquote prefixes each line with a quote marker. Filtering runs on your Mac and preserves the original clip.

## In the picker

The picker opens with a library sidebar. Click a collection or a library filter to narrow the list. Look for the leather folio for Work, the bookmarked journal for Personal, and the archive box for Pastebot imports. Other collections have tabbed folders with a color that stays consistent across launches. Rows show the clip and its source app icon. Choose **… → Get Info** for the source app name, last copied date and time, clip type, and collection. Text and links also show a character count. Switch to **Preview** in the same popover to see the content. The sidebar button beside Search switches between library and compact views and remembers your choice.

- Search by text, source app, or collection. Source logos help distinguish similar entries.
- Use a row’s **…** menu to preview, favorite, organize, or delete a clip.
- Choose **Paste as Plain Text** in a text or link’s row menu to paste without formatting.
- Open the gear to choose a shortcut, switch appearance, pause capture, or ignore an app.
- Click outside to dismiss. Capture continues in the menu bar until you quit.

<details><summary>Library and collection icons in light and dark</summary>

<img src="sidebar.png" width="300" alt="Library and collection artwork in both appearances, including a paper tray, brass star, photo print and chain links.">

</details>

## What is stored

Your history stays in `~/Library/Application Support/PasteNest/`. The app uses no account or cloud service. It skips secure input, excluded sources, and clipboard items marked private or transient. History files are owner-readable and are not encrypted by the app. Mac backups can include them.

By default, recent history lasts 30 days with a limit of 500 unprotected items. Favorites and collections persist until you remove them. If you previously imported a Pastebot library, its separate local snapshots remain after clearing the searchable history.

## Verify the download

From the directory containing the downloaded ZIP and checksum file, run:

```sh
shasum -a 256 -c SHA256SUMS.txt
```

This repository distributes compiled releases and documentation. The application source is private.
