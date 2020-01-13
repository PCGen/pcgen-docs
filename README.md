# About
 
This is the documentation for PCGen.
 
The original documentation, in HTML format, has been converted to Markdown, which is much easier to edit.
 
The Markdown-formatted text is compiled using Hugo, an excellent "static site generator". The output is a complete HTML website which can be browsed from a hard drive, or uploaded to a webserver.
 
# Instructions
 
 1. Install [Hugo](https://gohugo.io):
      * [Hugo Docs - Installing Hugo](http://gohugo.io/overview/installing/)
 2. Install [git](https://git-scm.com):
      * [git downloads](https://git-scm.com/downloads)
      * [git Handbook - Getting Started - Installing git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
 3. Download a copy ("clone") of the `pcgen-docs` repository to your computer.
      * i.e. to make a copy to C:/pcgen-docs/, you would do:
 
        `git clone --recursive https://github.com/PCGen/pcgen-docs.git C:/pcgen-docs/`
 
        Note the `--recursive` option is required to download the website theme, which is a "sub-module" of the main repository.
 
 4. Start the Hugo test server:
 
      * Go to the directory where you cloned the `pcgen-docs` repository:
 
        `cd G:/pcgen-docs`
 
      * Run Hugo in server mode:
 
        `hugo server`
 
      * Open a web browser to `http://localhost:1313`
 
      * Try changing a file in `content/`. Your web browser will automatically refresh, showing the changes!
 
 5. Compile the website, ready to upload to a webserver, or to include with PCGen:
 
      * Go to the directory where you cloned the `pcgen-docs` repository:
 
        `cd G:/pcgen-docs`
 
      * Run Hugo, putting the output into folder `G:/compiled-website`:
 
        `hugo --stepAnalysis -d G:/compiled-website/`
 
        The `--stepAnalysis` shows you how long each step took (in seconds), and how much RAM was used.
 
      * Find `G:/compiled-website/index.html` and double click it. It will open in a web browser. It should look exactly the same as the test server!
