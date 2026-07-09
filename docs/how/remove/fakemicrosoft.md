# Removing the Fake Microsoft Scam Prompts
## What is the fake Microsoft scam?
!!! warning
	Microsoft will **never** warn you about an issue and prompt you to call them to fix it. Legitimate Windows issues, if not fixed automatically, may be brought to your attention, and you may be prompted to manually investigate or take action.

	Do not call the phone number provided. Should you have called the phone number provided, they will ask you to install remote access software to "fix" the problem, which gives them persistent access to your computer, and collect money, data, etc.

The classic fake Microsoft scam is designed to look, at first glance, like an error on your computer, prompting you to call a phone number to fix the "issues" so that the scammers can scam you out of money to fix an issue you do not have.

!!! quote
	Cons don't fool us because we're stupid. They fool us because we're *human*.

	<div style="text-align:right">~ Brian Brushwood</div>

## How the scam starts
The scam is presented in many ways. They're always hosted as some sketchy website. You may find these posing as legitimate Google results, or perhaps someone on social media sends you a "news article" that you need to check out. Regardless, opening these links redirects you to the scam.

Web pages by definition, have 3 "languages" that the code is written in to make them operate. Two of these handle content, structure, and visual appearance. The third language, JavaScript, is used often to make things on a web page happen dynamically, such as opening a dialog when you click a button.

Web pages by default have JavaScript functions that define what happens when the page opens, closes, and many other things. However, it is possible to redefine these functions to be whatever you would like. These scam pages are designed to mimic errors on your computer, and not look like a web page, so they do two things that normal web pages don't:

- The **page load** function is defined to automatically set your browser to full screen, so that you don't see the browser, taskbar, or other applications, and the webpage takes up your whole screen.
- The **page close** function is redefined to do *nothing*, which prevents the web page from being closed gracefully.

## The fix
It's typically trivial to exit the fullscreen mode in your browser. This is normally done by pressing `F11` on your keyboard, unless this has been remapped to something else. Regardless of the fullscreen status, the close override will prevent you from closing the browser tab, or the browser, using the `X` in the top right corner. To fix this, do the following:

1. Press `Ctrl + Alt + Delete` and you'll see a screen pop up with several options.
2. Select `Task Manager`. In the window that pops up, on the **Processes** screen, you'll see two sections, labeled **Apps** and **Background processes**. The **Apps** are all of the applications that you have open, that are visible to you.
3. In the list of apps, find your web browser in this list (Edge, Chrome, Firefox, etc.). You can force close the app in one of two ways:

	a. Click on the browser in the apps list to select it, and in the top navigation bar, click on `End Task`.

	b. Right click on the browser in the apps list, and select `End Task` from the menu that pops up.

!!! warning
	When reopening your browser, you may see a prompt informing you that the browser closed unexpectedly, and offer to restore the pages you had open. **Do not restore** the pages, as this will pull up the problematic page again. Simply dismiss the prompt without restoring the session.

## Why this works
The webpage is telling the browser to do nothing when closing the page, as opposed to the default action of actually closing the page. While this means that you can't normally close the browser tab, or the browser, task manager overrides this.

When closing the browser with the `X`, Windows asks the browser to finish what it's doing, and gracefully shut down. This doesn't work, because the web page is preventing you from closing it, so the browser will never close, as the page is keeping it open.

When you use task manager, you're not closing the browser gracefully. By hitting `End Task`, Windows is instead forcefully terminating the process, regardless of whatever it's in the middle of. This is the reason you may see the warning about how it shut down unexpectedly.