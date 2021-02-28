# How Docsify Structures Data
Docsify uses a rather simple and easy way to structure the data for your website between one configuration file and keeping your data in the Markdown files.

## Configuration
Everything begins with the `index.html` file which tells the browser to use Docsify with this line `<script src="//cdn.jsdelivr.net/npm/docsify@4"></script>`. In this file you can also see that there's a line in one of the script tags that says `window.$docsify`. Under here we can list out all sorts of specifications for configuring your Docsify site. For this sample site, I use:
>loadSidebar: true,
>
>subMaxLevel: 2

which allows me to configure how the heading tags affect the side bar and to load the sidebar.

## Markdown Data
Once you're done with your configuration, all you have to worry about is your file structure and Markdown pages. Your initial homepage will always be set as `README.md` which can be changed with configuration, but is the standard for Docsify, as it will show your homepage on your GitHub. If you want to add additional pages, you need to create a `_sidebar.md` file to tell the sidebar how to navigate to each file. 

![](docs/sidebar.png)

Before you can tell the sidebar how to link pages, it is best to set up your file structure, so you know where each page is going to be locating. Take this example from the Docsify Documentation as an example for a file structure you can use if you are nesting your files in folders:

![](Capture.png)

Also here's an example of what my very simple file structure for this website looks like:

        .
        └── docs
            ├── README.md
            ├── prosandcons.md
            ├── alternatives.md
            ├── data.md
            └── video.md

Beyond your configuration and structure of your file system, there's not much else to using Docsify. You can add different themes like I did for this site in the `index.html` file, and you can set up different APIs and open-source plugins. When it comes down to it though, Docsify simply takes your markdown files, index.html and your _sidebar.md to compile them into a website without generating static html pages.
