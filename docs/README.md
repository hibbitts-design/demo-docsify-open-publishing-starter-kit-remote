# Remote Docsify

This site, which is built using [Docsify](https://docsify.js.org) and based on the [Docsify Open Publishing Starter Kit Remote template](https://github.com/hibbitts-design/docsify-open-publishing-starter-kit-remote), provides a quick way to render and share a remote Markdown file as a standalone page.

## Examples

* [Docsify Open Publishing Starter Kit README file](https://github.com/hibbitts-design/docsify-open-course-starter-kit/blob/main/README.md), displayed as a [Standalone Page](https://hibbitts-design.github.io/docsify-open-publishing-starter-kit-remote?basePath=https://raw.githubusercontent.com/hibbitts-design/docsify-open-course-starter-kit/main&standalone=true)
* [Docsify Open Publishing Starter Kit README file](https://github.com/hibbitts-design/docsify-open-course-starter-kit/blob/main/README.md), displayed as a [Standalone Page with a Table of Contents](https://hibbitts-design.github.io/docsify-open-publishing-starter-kit-remote?basePath=https://raw.githubusercontent.com/hibbitts-design/docsify-open-course-starter-kit/main&standalone=true&toc=true)
* [Single Page Docsify Open Course Starter Kit](https://github.com/paulhibbitts/cpt-363-user-interface-design/blob/main/README.md), displayed as a [Standalone Page with a Table of Contents](https://hibbitts-design.github.io/docsify-open-publishing-starter-kit-remote?basePath=https://raw.githubusercontent.com/paulhibbitts/cpt-363-user-interface-design/main/&toc=true#/)

## Technical Details

This is a customized [Docsify Open Publishing Starter Kit](https://github.com/hibbitts-design/docsify-open-publishing-starter-kit) site configured to render remote Markdown files via URL parameters in the format `https://hibbitts-design.github.io/docsify-open-publishing-starter-kit-remote?basePath=URLpath&homepage=filename.md`. The **basepath** parameter is the directory containing the raw source Markdown file to render. If the file is named the expected default **README.md** then no other parameter are required, otherwise the **homepage** parameter must also be included set to the name of the file to render. To render a file stored on GitHub you need to use the raw source URL of a file (i.e. raw.githubusercontent.com), tap the **Raw** button when [viewing a file](https://docs.github.com/en/repositories/working-with-files/using-files/viewing-a-file) to get this URL.  

For example, to render the Markdown file **[README.md](https://github.com/hibbitts-design/docsify-open-course-starter-kit/blob/main/README.md)** (the expected default name) as a standalone page the URL would be:  
https://hibbitts-design.github.io/docsify-open-publishing-starter-kit-remote/?basePath=https://raw.githubusercontent.com/hibbitts-design/docsify-open-course-starter-kit/main/

To render the Markdown file **[README.md](https://github.com/hibbitts-design/docsify-open-course-starter-kit/blob/main/README.md)** (the expected default name) as a standalone page with a table of contents the URL would be:  
https://hibbitts-design.github.io/docsify-open-publishing-starter-kit-remote/?basePath=https://raw.githubusercontent.com/hibbitts-design/docsify-open-course-starter-kit/main/&toc=true

To render the Markdown file **[introduction.md](https://github.com/hibbitts-design/docsify-open-publishing-starter-kit/blob/main/docs/introduction.md)** as a standalone page, the URL would be:  
https://hibbitts-design.github.io/docsify-open-publishing-starter-kit-remote/?basePath=https://raw.githubusercontent.com/hibbitts-design/docsify-open-publishing-starter-kit/main/docs&homepage=introduction.md

To render the Markdown file **[introduction.md](https://github.com/hibbitts-design/docsify-open-publishing-starter-kit/blob/main/docs/introduction.md)** as a standalone page with a table of contents, the URL would be:  
https://hibbitts-design.github.io/docsify-open-publishing-starter-kit-remote/?basePath=https://raw.githubusercontent.com/hibbitts-design/docsify-open-publishing-starter-kit/main/docs&homepage=introduction.md&toc=true

_TIP: To get the path of a file on GitHub for the **basepath** URL parameter, tap the **Raw** button when viewing the file and then remove the filename. If not a README file, the filename will need to be passed using the **homepage** URL parameter._

## Troubleshooting

_Updated Markdown file not displayed in the Browser._  
Docsify is likely displaying the last cached version. To ensure the most recent version of a file is loaded, do a [hard refresh of your Browser cache](https://www.makeuseof.com/hard-refresh-browser/).

_Embedded image not displayed as expected._  
The most likely cause for embedded images not being displayed as expected is the use of HTML (i.e. `<img src="images/filename.jpg" alt="Alt Text">`). Use Markdown for embedded images if possible (i.e. `![Alt Text](images/filename.jpg)`) to better support remote rendering.

_Embedded iFrame not displayed as expected._   
Due to iframe cross-domain issues embedded content may not be able to be displayed. Use the included rich media embed service [embed.ly](https://embed.ly/) as a workaround.  

For example, the following iFrame HTML:  

```
<div class="video-container-16by9"><iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRnnRFelgw1ksq_p8Eryg3dnyLCRRLPf5fBgdwdv9p-tCIwcxqWvzDGrGbjxGHL7HqEJVpmV26ntk3a/embed?start=false&loop=false&delayms=3000" frameborder="0" width=780" height="585" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe></div>
```

Would be changed to:  

```
<a class="embedly-card" data-card-controls="0" data-card-align="left" href="https://docs.google.com/presentation/d/1BLaaOTsGxDmNcAhg6pdx3hl9IvI8NErg8Oe5ceh83fw/edit?usp=sharing">Grav and Docsify Slides Placeholder</a>
```

---

**🙇🏻‍♂️Credits**  
[Beau Shaw](https://github.com/DaddyWarbucks) for his [Remote Docsify](https://github.com/DaddyWarbucks/remote-docsify) example.  
[Alan Levine](https://github.com/cogdog) for the inspiration of a consolidated ReadMe collection.