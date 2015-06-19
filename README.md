ext-src-path
============

An extension to point to the source location of Google Chrome extentions

Description from the Webstore (https://chrome.google.com/webstore/detail/extension-source-locator/cmhbfegjgncgaikpopenldnaidbhdopp):
Would you like to see how popular extensions have implemented a feature? Tired of looking for the extension ID to construct the path that will lead you to the source?

This is the extension for you!

Features:
Replaces the functionality of the New Tab
Lists all installed extensions with their icons next to it
Allows to copy to the clipboard the extension path

---

In my system, the extension is installed in `~/.config/chromium/Default/Extensions/` . So I modified the js file in line 36.(**I use the absolute path because the `~` sometimes doesh't work.**)

At first , I want it can open the folder manager with clicking the extension name, but I haven't got any way to achieve it.

Then I want it can open the folder in the tab, and I tried to modify `href` of `a` but chromium-browser said **Not allowed to load local resource:**.

At last I add each `a` an `id` and use jQuery to append `click()` response. As the change you can see in the code.
