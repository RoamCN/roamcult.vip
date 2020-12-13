- Roam Research的JS支持能做的事情远远超过了我的想象。其中一个最符合我使用的案例就是用JS来激活关键词，自动填充模版。步骤如下：
- 
- 如果你已经使用了[Roam42](https://www.roamstack.com/roam42)，你可以跳过前5步，直接从第六步开始。 
- 最近，我们注意到了另一种扩大文本的方法。 Roaman 同事 [Victor Tabori](https://twitter.com/ViktorTabori)编写了一个漫游插件，使我们能够在漫游中直接设置文本扩展器。 它可以与 JavaScript 配合使用，而 JavaScript 听起来比实际复杂得多。
- 
- 配套教学视频YouTube video by Les Kristofs https://youtu.be/aJEqN98j2W4

## Table of Contents
    - [An introduction to Roam-flavored Markdown](https://www.roamstack.com/templates/[intro-markdown](../intro-markdown.md))
    - [Why use text templates?](https://www.roamstack.com/templates/[why-text-templates](../why-text-templates.md))
    - [Create your own Roam shortcodes that turn into templates](https://www.roamstack.com/templates/[text-expander-choices](../text-expander-choices.md))
    - [System-wide text expansion](https://www.roamstack.com/templates/[system-wide-text-expansion](../system-wide-text-expansion.md))
    - [Browser-wide text expansion](https://www.roamstack.com/templates/[browser-wide-text-expansion](../browser-wide-text-expansion.md))
    - [Roam-wide text expansion](https://www.roamstack.com/templates/[roam-wide-text-expansion](../roam-wide-text-expansion.md))
    - [Low-tech: copy-paste](https://www.roamstack.com/templates/[low-tech-copy-paste](../low-tech-copy-paste.md))
    - [Text template examples](https://www.roamstack.com/templates/[text-template-examples](../text-template-examples.md))
- **Step 1: Create roam/js page**
    - From any page in Roam, create a page titled roam/js by typing [leodknuth插件集合](../leodknuth插件集合.md).

## []()An introduction to Roam-flavored Markdown
- **Step 2: Enable JavaScript on roam/js page**
    - Click the link so you’re on the roam/js page. There, enable JavaScript by typing {{[leodknuth插件集合](../leodknuth插件集合.md)}}
    - 
    - ![roam/js page](https://www.roamstack.com/wp-content/uploads/roamjs-page.png)
- Markdown is a way to add formatting to plain text in a way that can be interpreted by text editors (like Roam). Mastering Markdown is easy and sets you on the path of becoming a keyboard-first user, which will speed up your workflow a lot.
- **Step 3: Create a code block below the JavaScript block**
    - Hit Enter and then Tab to create a child block under the JavaScript block. Now, we’re going to add a code editor.
    - In the new block, type /code and select the Code Block option from the trigger menu. Alternatively, type six backticks (```javascript
```).
    - ![Roam code block via trigger](https://www.roamstack.com/wp-content/uploads/codeblock-trigger-700x356.png)
    - Or:
    - ![Roam code block via shortcode](https://www.roamstack.com/wp-content/uploads/codeblock-shortcode-700x196.png)
    - Click outside the block to show the code editor and set the language to JavaScript via the dropdown.
    - ![Roam codeblock set to JavaScript](https://www.roamstack.com/wp-content/uploads/codeblock-javascript-700x305.png)
- If you’re going to use text templates that you create outside Roam (using an app or browser extension), you’ll need Markdown. If you’re going for the “Roam-native” expansion plugin we’re teaching you later, you can directly style your templates in Roam.
- **Bold****
- **Step 4: Add plugin to code block**
    - Now, go to Viktor Tabori’s [Github page](https://gist.github.com/thesved/79371d0c1dd34b6750c846368b323113) to get the code of the plugin. Copy everything from */ to the final } (don’t include the last three backticks (```)):
    - ![](https://www.roamstack.com/wp-content/uploads/begin-viktor-snippet-700x135.png)
    - …
    - ![](https://www.roamstack.com/wp-content/uploads/end-viktor-snippet-700x106.png)
- __Italics____ (double underscore)
- **Step 5: Enable JavaScript**
    - Now that everything is ready, click the ![Roam JavaScript activation button](https://www.roamstack.com/wp-content/uploads/javascript-button.png) button to activate the plugin.
    - Now, the block becomes yellow, indicating the code is being used by Roam. We can now set up our text templates!
    - ![JavaScript activated in Roam](https://www.roamstack.com/wp-content/uploads/javascript-activated-700x227.png)
    - **Step 6: Set up text templates**
    - From any page, create a link that starts with the template/ namespace. Any word that comes after the / will become your shortcode for text on that page.
    - For example, if I create a page titled __template/book__, every time I type :book: it pastes all text that’s on the __template/book__ page.
    - ![Roam book template](https://www.roamstack.com/wp-content/uploads/book-template-540x600.png)
    - Now see it expand when I type :book:
    - ![Expanding Roam template animation](https://www.roamstack.com/wp-content/uploads/book-template-expansion.gif)
- ~~Strikethrough~~~~
- Highlight^^
- Heading 1 *#
- Heading 2 *##
- Heading 3 *###
- __* These shortcodes only work in text templates, not when directly typed in Roam.__

## Why use text templates?
- Roam has no inherent structure as it’s a tool for networked thinking; each block can connect to every block. But, there is some hierarchy on a page level; the way blocks are placed.
- Many Roamans plan their pages with attributes and headings, to give their system some structure and make it easier to retrieve notes. But having to type the same thing again and again is wasteful. A programmer wouldn’t do that, and we’re here to become programmers of thoughts.
- Early on, Roamans started to keep pages of text snippets that they use often. As Roam’s markup information is all in characters you can type, people could go completely wild.
- Before long, other people pointed to text expanders, and now thousands of Roamans are creating their own Roam shortcuts each day. Some have 1000-character templates that they trigger with three keystrokes; the possibilities are almost endless.
- We will now cover a few ways to reduce typing in Roam. Then, we share snippets we use ourselves so you get an idea of what’s possible.

## []()Create your own Roam shortcodes that turn into templates
- Now that you understand the power of text templates, let’s dive into the different ways to set up some automation for them. There are three ways, each requiring different tools and knowledge:
    - System-wide: apps
    - Browser-wide: extensions
    - Roam-wide: JavaScript.
- We’ll discuss each option briefly, starting with system-wide apps. Then, we move to the browser, and finish by walking you through an implementation specifically for Roam. Each approach has its advantages and disadvantages. Pick one:
    - If you want to have access to templates on your whole system, go for a proper text expander app (requires a purchase).
    - If you’re likely to use templates on other websites too, go for the browser extension.
    - If you’re strapped for cash and are only likely to use shortcuts in Roam, go for the templates in Roam.

## []()System-wide text expansion
- In this category, we see famous apps like [Alfred](https://www.alfredapp.com/) (Mac) and [TextExpander](https://textexpander.com/) (Mac, Windows, and mobile). The advantage of using a text expansion __app__ is that you can use it anywhere on your system.
- Want to set up templates for Word? Or email templates for Outlook? Use an app. You’ll be able to set up simple text templates, but they also have dynamic fields to insert other data—think of the time, date, or manual inputs.
- If you go with TextExpander, your snippets will sync across all your devices. However, this costs you a yearly fee of $40. If you’re a Mac user and only need to have text templates on one device, Alfred is probably a better option with its one-time fee.

## []()Browser-wide text expansion
- We don’t have a lot of experience in the area of browser-based text expanders, but one tool that keeps popping up on our radar is [Text Blaze](https://chrome.google.com/webstore/detail/text-blaze/idgadaccgipmpannjkmfddolnnhmeklj). This is a free extension (while still in beta) that works in Chromium browsers (Chrome, Edge, Brave, Vivaldi).
- Text Blaze works the same as system-wide apps, but only in your browser. Given that Roam currently is a web app, Text Blaze will be enough for most users.

# Backlinks
## [📘教程](📘教程.md)
- [用roam/js创建和使用模版](../用roam/js创建和使用模版.md)

- [用roam/js创建和使用模版](../用roam/js创建和使用模版.md)f

