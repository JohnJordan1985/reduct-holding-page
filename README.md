# Reduct.blog


## Including scripts on a page
To include scripts on a page, do the following:<ol>
<li style="margin-bottom: 0.5rem">in **index.shtml** of page, use SSI to add link to scripts index in **head** of page, e.g. after the `title` attribute:
<br/>`<!--#include virtual="scripts/index.html" -->` 
</li>
<li style="margin-bottom: 0.5rem">in **scripts/index.html** list the scripts you want to load, as externally loaded files using the `script` tag with the `defer` attribute:<br/>`<script src="scripts/main.js" defer></script>`
<br style="margin-top: 0.5rem"/>Note: the URL for the script is **relative to the page's index.shtml file**
</li>
<li style="margin-bottom: 0.5rem">in the actual script file, place the script to be excecuted, as per usual.</li>
</ol>

## Adding a new page
Copy the pre-existing "new" page from the "template" directory, in the root of the server
- Set the value of the `pathToMainContent` variable to the relative path to the "content" folder that contains content specific to the page, when taking the starting point to be the `body.shtml` file contained within the `common-content`, which sits at the server root.

- Set all the values of the paths to the `common-content` folder, which sits at the server root. 


- Add page content to the `main-content.html` file, and page styles to the `page-styles.html` file

## Notes
Markdown preview can be triggered in Sublime 3 using `alt + m`, following advice here: https://packagecontrol.io/packages/MarkdownLivePreview.