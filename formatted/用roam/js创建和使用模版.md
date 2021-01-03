- Roam Research的JS支持能做的事情远远超过了我的想象。其中一个最符合我使用的案例就是用JS来激活关键词，自动填充模版。步骤如下：
- 如果你已经使用了[Roam42](https://www.roamstack.com/roam42)，你可以跳过前5步，直接从第六步开始。 
- 最近，我们注意到了另一种扩大文本的方法。 Roaman 同事 [Victor Tabori](https://twitter.com/ViktorTabori)编写了一个漫游插件，使我们能够在漫游中直接设置文本扩展器。 它可以与 JavaScript 配合使用，而 JavaScript 听起来比实际复杂得多。
- 配套教学视频YouTube video by Les Kristofs https://youtu.be/aJEqN98j2W4
- **Step 1: Create roam/js page**
    - From any page in Roam, create a page titled roam/js by typing [leodknuth插件集合](../leodknuth插件集合.md).
- **Step 2: Enable JavaScript on roam/js page**
    - Click the link so you’re on the roam/js page. There, enable JavaScript by typing {{[leodknuth插件集合](../leodknuth插件集合.md)}}
    - 
    - ![roam/js page](https://www.roamstack.com/wp-content/uploads/roamjs-page.png)
- **Step 3: Create a code block below the JavaScript block**
    - Hit Enter and then Tab to create a child block under the JavaScript block. Now, we’re going to add a code editor.
    - In the new block, type /code and select the Code Block option from the trigger menu. Alternatively, type six backticks (```javascript
```).
    - ![Roam code block via trigger](https://www.roamstack.com/wp-content/uploads/codeblock-trigger-700x356.png)
    - Or:
    - ![Roam code block via shortcode](https://www.roamstack.com/wp-content/uploads/codeblock-shortcode-700x196.png)
    - Click outside the block to show the code editor and set the language to JavaScript via the dropdown.
    - ![Roam codeblock set to JavaScript](https://www.roamstack.com/wp-content/uploads/codeblock-javascript-700x305.png)
- **Step 4: Add plugin to code block**
    - Now, go to Viktor Tabori’s [Github page](https://gist.github.com/thesved/79371d0c1dd34b6750c846368b323113) to get the code of the plugin. Copy everything from */ to the final } (don’t include the last three backticks (```)):
    - ![](https://www.roamstack.com/wp-content/uploads/begin-viktor-snippet-700x135.png)
    - …
    - ![](https://www.roamstack.com/wp-content/uploads/end-viktor-snippet-700x106.png)
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

# Backlinks
## [📘教程](📘教程.md)
- [用roam/js创建和使用模版](../用roam/js创建和使用模版.md)

- [用roam/js创建和使用模版](../用roam/js创建和使用模版.md)f

