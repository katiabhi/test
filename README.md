# Introduction to Make it mine journey


## Basics

* The solutions are singleton in nature i.e. preferrably one deployment should be modified by one user at a time.
* Follow the below steps to open your previous workspace?
    * <walkthrough-editor-open-file> open a file for editing</walkthrough-editor-open-file>
  

**h2**: text

Click  **abc** button

## page 2

hyperlink [demo](https://google.com).




## page 3

Try running a command now:
```bash
echo "Hello World"
```

**Tip**: Click the copy button on the side of the code box and paste the command in the terminal to run it.


## page 4


*  To , open the editor by clicking on the <walkthrough-cloud-shell-editor-icon></walkthrough-cloud-shell-editor-icon> icon.
*  open `README.md`.
*  Try making a change to the file for this tutorial, then saving it using the <walkthrough-editor-spotlight spotlightId="fileMenu">file menu</walkthrough-editor-spotlight>.

To restart the tutorial with your changes, run:
```bash
cloudshell launch-tutorial -d tutorial.md
```


## Special tutorial features

In the Markdown for your tutorial, you may include special directives that are specific to the tutorial engine. These allow you to include helpful shortcuts to actions that you may ask a user to perform.


### Trigger file actions in the text editor
To include a link to <walkthrough-editor-open-file filePath="cloud-shell-tutorials/tutorial.md">open a file for editing</walkthrough-editor-open-file>, use:

```
<walkthrough-editor-open-file
    filePath="cloud-shell-tutorials/tutorial.md">
    open a file for editing
</walkthrough-editor-open-file>
```


### Highlight a UI element

You can also direct the user’s attention to an element on the screen that you want them to interact with.

You may want to show people where to find the web preview icon to view the web server running in their Cloud Shell virtual machine in a new browser tab.

Display the web preview icon <walkthrough-web-preview-icon></walkthrough-web-preview-icon> by including this in your tutorial’s Markdown:

```
<walkthrough-web-preview-icon>
</walkthrough-web-preview-icon>
```

To create a link that shines a <walkthrough-spotlight-pointer spotlightId="devshell-web-preview-button">spotlight on the web preview icon</walkthrough-spotlight-pointer>, add the following:

```
<walkthrough-spotlight-pointer
    spotlightId="devshell-web-preview-button">
    spotlight on the web preview icon
</walkthrough-spotlight-pointer>
```

You can find a list of supported spotlight targets in the [documentation for Cloud Shell Tutorials](https://cloud.google.com/shell/docs/tutorials).

You've now built a tutorial to help onboard users!

Next, you’ll create a button that allows users to launch your tutorial in Cloud Shell.


## Creating a button for your site

Here is how you can create a button for your website, blog, or open source project that will allow users to launch the tutorial you just created.


### Creating an HTML Button

To build a link for the 'Open in Cloud Shell' feature, start with this base HTML and replace the following:

**`YOUR_REPO_URL_HERE`** with the project repository URL that you'd like cloned for your users in their launched Cloud Shell environment.

**`TUTORIAL_FILE.md`** with your tutorial’s Markdown file. The path to the file is relative to the root directory of your project repository.

```
<a  href="https://console.cloud.google.com/cloudshell/open?git_repo=YOUR_REPO_URL_HERE&tutorial=TUTORIAL_FILE.md">
    <img alt="Open in Cloud Shell" src="http://gstatic.com/cloudssh/images/open-btn.png">
</a>
```

Once you've edited the above HTML with the appropriate values for `git_repo` and `tutorial`, use the HTML snippet to generate the 'Open in Cloud Shell' button for your project.


### Creating a Markdown Button

If you are posting the 'Open in Cloud Shell' button in a location that accepts Markdown instead of HTML, use this example instead:

```
[![Open this project in Cloud Shell](http://gstatic.com/cloudssh/images/open-btn.png)](https://console.cloud.google.com/cloudshell/open?git_repo=YOUR_REPO_URL_HERE&page=editor&tutorial=TUTORIAL_FILE.md)
```

Likewise, once you've replaced `YOUR_REPO_URL_HERE` and `TUTORIAL_FILE.md` in the 'Open in Cloud Shell' URL as described above, the resulting Markdown snippet can be used to create your button.


## Congratulations

<walkthrough-conclusion-trophy></walkthrough-conclusion-trophy>

You’re all set!

You can now have users launch your tutorial in Cloud Shell and have them start using your project with ease.
