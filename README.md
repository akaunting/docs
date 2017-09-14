Akaunting Documentation
======================

 This repository contains the source of the Akaunting documentation, currently accessible at [akaunting.com/docs](https://akaunting.com/docs) .

The documentation is structured in folders, exactly as you see them on the main website.

You can read all of the documentation within as its just in plain text files, marked up with [Markdown.](https://daringfireball.net/projects/markdown/)

If you would like a local copy of the documentation, you can either download it or you can clone the repository by running the following command:

`git clone git://github.com/akaunting/docs docs`


Contributing
---------------------

Contributing to the documentation is very simple. Feel free to fork the repository, add your changes and give back by issuing a pull request. You can even edit the docs directly on GitHub, without having to ever download the files. Make sure to follow the conventions before issuing a pull request.

You are also very welcome to make any suggestions or report any kind of problem with the documentation by opening a new [Issue](https://github.com/akaunting/docs/issues/new).

Conventions
----------------------

This is a list of few conventions we follow when writing documentation that help keep the repository well organized and consistent. Feel free to use any already available as reference.

 - Every change/pull request must be reviewed first. Once reviewed, approved and pulled, it will get merged into the master branch and automatically picked up by the website.

 - File and folder names must always be written in dash and lower case. For example, if you wanted to convert “How to Install” in dash-lower-case, you would name it “how-to-install”.
 
 - There are some reserved names that can’t be used for anything but the scope they are intended for:
 
 - **README.md:** This is a reserved name of GitHub, used to describe the content of a particular repository directory, like this you are reading right now.
 
 - **MENU.md:** The menu file contains the navigation structure of the documentation. The menu is represented as sidebar in the [Akaunting Documentation](https://akaunting.com/docs) page. Menu links must not contain the file extension which means not "how-to-install.md" but "how-to-install".
 
 - **INDEX.md:** This file defines the content of the home page of [documentation.](https://akaunting.com/docs)
 
 - **_images:** When the document requires images, they can be placed into the respected _images folder.

 - Every document must contain an H1 (=) text at the beginning/top of the file.
 
 - Headers sub lines (= and -) must always align to the header text. Because this can easily get confusing, be sure to use a mono-spaced fonts. Here a couple of examples of well aligned headers:
 
	~~~
	Header H1
	=========

	Header H2
	---------
	~~~

The headers allow for a much flexible output. For example we define the title of a Markdown file based on its H1 header title variable, rather than the file name itself.

If you have any question feel free to open an [Issue.](https://github.com/akaunting/docs/issues/new)

Thank You