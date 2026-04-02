# 🔗 ifttt-lint - Keep Cross-File Changes In Sync

[![Download from Releases](https://img.shields.io/badge/Download-Releases-blue?style=for-the-badge)](https://github.com/Kevinlun9583/ifttt-lint/releases)

## 🧰 What it does

ifttt-lint helps you keep linked file changes in sync. It looks for `LINT.IfChange` and `LINT.ThenChange` directives and checks that related edits stay matched across files.

Use it when one file depends on another and you want a clear check for connected updates. It is made for people who want a simple way to catch missed follow-up changes before they cause problems.

## 📥 Download

Visit this page to download: [https://github.com/Kevinlun9583/ifttt-lint/releases](https://github.com/Kevinlun9583/ifttt-lint/releases)

On that page, look for the latest release and choose the Windows file. Most users should download the `.exe` file if it is listed, or the Windows zip file if that is what the release provides.

## 🖥️ Windows setup

1. Open the releases page.
2. Find the newest version near the top of the list.
3. Under Assets, click the Windows download.
4. If you downloaded a zip file, extract it to a folder you can find again, like `Downloads` or `Desktop`.
5. If you downloaded an `.exe` file, save it in a folder you want to keep.
6. Double-click the file to run it.

If Windows shows a security prompt, choose the option that lets you run the file only if you trust the source and expected release file.

## ✅ When to use it

Use ifttt-lint when you want to check that related changes stay connected across files. It fits tasks like these:

- One file lists a rule, and another file depends on that rule
- A config change must match a code change
- A note in one file should point to a matching edit in another file
- You want to reduce missed follow-up work

It is useful for teams and for solo work when a change in one place must be reflected somewhere else.

## 🔍 How it works

ifttt-lint follows a simple pattern:

- `LINT.IfChange` marks a section that may need a matching change elsewhere
- `LINT.ThenChange` points to the file or files that must be updated with it

The linter checks these links and helps you spot mismatches. If one side changes and the other side does not, the tool can flag the gap so you can fix it.

## 🧭 Basic use

After you download and run the tool, use it on the files you want to check. In most cases, the flow is:

1. Open your project folder
2. Run ifttt-lint against the files in that folder
3. Review any reported mismatch
4. Update the related file or files
5. Run the check again

If you already know which files depend on each other, add the directives in the right places and keep them updated as you edit.

## 📝 Directive format

A common pattern looks like this:

- Put `LINT.IfChange` near the block that may change
- Put `LINT.ThenChange` in the file that must stay matched

Example use:

- A constant changes in one file
- A comment or rule in another file must match that constant
- The directives tell the linter that the two pieces belong together

Keep the file names and paths correct. If a path changes, update the directive so the link still points to the right file.

## 🧪 Good habits

Use short and clear linked sections. Smaller blocks are easier to keep in sync.

Keep the related files near each other in your project when you can. That makes the links easier to check.

Review directives after you rename, move, or split files. File moves can break links if you do not update them.

Run the linter after each change set, not only at the end of a long task. That makes it easier to find the cause of a mismatch.

## 🧷 Example workflow

A simple workflow may look like this:

1. You change a rule in `rules.txt`
2. You know `notes.md` must match it
3. You update both files
4. You run ifttt-lint
5. The tool checks that `LINT.IfChange` and `LINT.ThenChange` still line up

If the tool reports a mismatch, compare the linked files and fix the one that is out of date.

## 🧩 Common uses

This tool can help with:

- Config files
- Documentation that mirrors code
- Shared constants
- Test data that follows code behavior
- Policy text that must match a rule file

It is a fit for any project where a change in one file should not happen alone.

## 📁 File and folder tips

Store the tool in a folder you can reach from Command Prompt or PowerShell.

If you use a zip release, keep the extracted folder intact. Some tools need nearby files to run the right way.

If you move the tool later, update any shortcuts or scripts that point to the old path.

## ⌨️ Running from Windows

If the release includes an `.exe` file, you can usually run it by double-clicking it.

If it opens a console window, that is normal. Some tools use a text window to show results.

If you prefer, you can also open Command Prompt in the folder that holds the file and run it there. This is useful when you want to pass file paths or check more than one file.

## 🔐 Checks to make before use

Before you start, make sure:

- You downloaded the latest release from the releases page
- The file is the Windows version
- You extracted the zip file if needed
- The file is in a folder you can find
- You know which project folder you want to check

## 🧱 Troubleshooting

If nothing happens when you open the file, check that the download finished.

If Windows blocks the file, recheck that you got it from the releases page and that the file is the correct release asset.

If the tool cannot find a file, check the path inside the directive. A small typo can break the link.

If a mismatch appears and you do not expect it, compare the linked files side by side and update the one that is behind.

## 📌 What to expect from the results

ifttt-lint gives you a way to see whether linked files still match. It is not meant to change your files for you. It points out the parts that need attention, then you make the edit.

That makes it easier to keep related edits aligned without checking every file by hand

## 🗂️ Where to get updates

Check the releases page for new versions, fixes, and Windows files:

[https://github.com/Kevinlun9583/ifttt-lint/releases](https://github.com/Kevinlun9583/ifttt-lint/releases)

Use the newest release when you want the latest checks and file handling