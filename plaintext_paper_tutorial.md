#MVC Tutorial: a _PlainText_ paper on GitHub

How to use __Markdown__, __BibTeX__, and __Pandoc__ to efficiently write and publish an academic paper on __GitHub__.

G. E. Saretto - December 17th, 2014

> __GitHub__ is an excellent platform to store, access and edit your academic writing: it is an online database that allows you to track your notes and drafts, quantify your daily labor, and showcase or share your progression. The habit of recording and publishing every stage of your work quickly improves your sense of productivity, and the documents that you produce will always be easily accessible. Nevertheless, the integration between the various components that participate in the redaction of an academic text - notes, drafts, bibliography, polished work - can pose some problems. Here is a tutorial that will accompany you in every step of your work, from the collection of ideas to the final presentation of your paper.

##1. Setting up the environment

1. From your __GitHub__ [home page](https://github.com/), create a new repository by clicking on the dedicated [link](https://github.com/new). Use a simple, catchy name, so that the page will be easily accessible by your peers as well (e.g.: `sonnets_print` for a paper about Shakespeare's Sonnets as a reaction to the advent of printing), and provide a brief and clear description. Click on __Create Repository__ when you are done.

2. Create a _working folder_ on your hard drive; open the __terminal__ and access the folder where you usually store your work (e.g.: `/home/user/Documents/`) by using the `cd` (_change folder_) and `cd ..` (_go up one folder_) commands; here type ``mkdir sonnets/`` to create the folder (substitute ``sonnets`` with the working title for your project).

3. Access the folder by typing ``cd sonnets`` (substitute ``sonnets`` with the working title for your project).

3. Here create three files (substitute ``sonnets`` with the working title of your project):

	1. a __notes__ file, where you will keep track of ideas and _impromptu_ provisional passages - type ``touch sonnets_notes.md``;
	
	2. an __outline__ file, to start working on the structure of your paper - type ``touch sonnets_structure.md``;
	
	3. a __draft__ file, which will become your paper - type ``touch sonnets.md``.

4. Initiate a __Git__ repository in this folder: it will constantly keep track of your changes to every file. Type ``git init`` in the terminal to do so.

5. To verify that your folder has become a __Git__ repository, type ``git status``; as you will be able to read, the repository is waiting for something to commit.

6. __Add__ each of the three files contained in the folder (you can always check what's in it by typing ``ls``) to the current __stage__ of your work by using the command ``git add``, followed by the name of each file:
	
	1. for the __notes__, type ``git add sonnets_notes.md``;
	
	2. for the __outline__, type ``git add sonnets_structure.md``;
	
	3. for the __draft__, type ``git add sonnets_draft.md``.

		- __Tip__: if you want to add _every file_ in a folder to the folder's repository, you can simply type: ``git add -A``; remember, however, that this is not always necessary.

7. Now __commit__ your changes: the state of every file that you have added to the current __stage__ will be saved as part of a single set of _changes_, to which you will be able to add a brief annotation. In order to do so, type the command `git commit -m`, followed by your comment placed between quotation marks `" comment "`. This initial commit, for instance, might be something like: `git commit -m "Setting up the files for my paper on the Sonnets"`.

8. Finally, __push__ your changes to the _online_ repository: the package of changes that you have __committed__ (in the form of the individual files that you have __added__) will be uploaded on the GitHub platform, so that it will be accessible from any device. Our first __push__ is special: we have to tell our _local_ repository where to locate the _remote_ repository with which each change will be constantly coordinated. The empty online repository that you have created during step __1__ will probably contain a detailed set of instructions; in any case, only two commands are required for your __first__ push:
	
	1. define the _remote_ origin of your repository by typing the line `git remote add origin` followed by the `https://` web address of __your__ _online_ repository (e.g.: `git remote add origin https://github.com/gesaretto/sonnets_print.git`);
	
	2. upload your current committed __stage__ by typing ``git push -u origin master``.

3. All set! We have a _local_ repository, containing our __draft__, our __structure__, and our __notes__, and a mirroring _remote_ repository that will track every step of our work.

##2. Writing and tracking

1. The format that you will use for writing your paper is an accessible and versatile language called __Markdown__; you can find plenty of software to redact your __.md__ files online: [MarkdownPad](http://markdownpad.com/) for Windows and [ReText](http://sourceforge.net/projects/retext/) for Linux are user-friendly, free options that are appropriate for beginners, given their straightforward GUI. A few hints to get started (more info can be found on the language's [official page](http://daringfireball.net/projects/markdown/basics)):
	
	- to __emphasise__ your text, encompass it with one (for _italics_) or two (for __bold__) `*asterisks*` or `__underscores__`;
	
	- for __titles__, use `#hashtags`: the main titles of the paper will be preceded by one `#hashtag`, the title of each smaller section by `##two hashtags`, the title of each paragraph by `###three hashtags` and so on;
	
	- for __lists__ use either numbers followed by a dot and a space (`1. list item`), or asterisks (`* list item`) and dashes followed by a space (`- list item`);
	
	- for __footnotes__, use square brackets to create a __label__ that will follow the word requiring a note (e.g. `word[^note]`) - then, in a different paragraph, use the same __label__, followed by a _colon_, to write your actual note (e.g. `[^note]: This is a note.`)[^1-footnote];

	- if you need to quote pieces of `code` in your paper, simply use ticks (e.g.: `` `code` ``) to encompass them.

1. After each writing session, remember to __add__, __commit__, and __push__ your changes:
	
	1. __add__ each file that you have worked on to the current _stage_ by using the command `git add`, followed by the name of the file;
	
	2. __commit__ your changes with the `git commit` command, followed by a comment on the progression of your work placed in quotation marks after the flag `-m` (e.g.: `git commit -m "This is a comment on my work."`).
	
	3. __push__ your changes to the _remote_ repository by using the command `git push`; you will have to enter your username and password.
	
		- __Tip__: you can check the status of your repository (tracked and untracked changes and files) by typing `git status` at any time.

1. Follow and share the development of your work through the [GitHub](https://github.com/) dashboard.
			
[^1-footnote]: It is easier than it sounds!

##3. Managing your bibliography

1. The standard that you will use to manage your references, __BibTex__, is an   effective and flexible bibliographic system; the information needed for your paper will be stored in a single __.bib__ archive, a human-readable, adaptable format, compatible with several programs and textual file types. Download a manager for __BibTex__ online: [Zotero](https://www.zotero.org/) is a powerful option, although slightly overwhelming for beginners; we suggest the simple GUI of [JabRef](http://jabref.sourceforge.net/), available for most operating systems.

	- The use of __JabRef__ is very intuitive: create a new record for each reference, specify the appropriate type, fill in the required fields, add an abstract and a review whenever you feel it may be necessary (I find it useful to store relevant _quotations_ and _page numbers_ here, so that I don't have to rush to the library later).
		
		- __Tip__: entering each proper name in the format "_LastName, FirstName_" (e.g. "Vargas Llosa, Mario") will avoid confusion.
	
		- __Tip__: the __BibTex Key__ that we will discuss later is always visible as the last entry in each record; a "Generate BibTex key" command is available (the small wand on the left column, in the lower section of the window).

		- __Important__: in order to easily use your bibliographic archive across different systems, set the __Default encoding__ as __UTF8__ from the __Options__ - __Preferences__ panel; please note that this is an __essential requirement__ to let your __.bib__ file work with __Pandoc__.

2. Keep your bibliographic archive constantly updated. The __.bib__ file where your references are stored should be placed inside of your working folder (e.g.: `sonnets.bib`), so that you may easily __add__, __commit__, and __push__ your bibliographic data and notes together with the rest of your documents.

3. Learn to recognize the __BibTex Key__ of each entry: it is usually a combination of the author's last name and the book's year of publication (e.g.: `VargasLlosa1975` for Mario Vargas Llosa's _La Orgía Perpetua_); this functions as a __label__ to identify the entire set of data related to a reference.

4. To insert a reference to an entry of your __.bib__ archive within your __.md__ document, simply use the corresponding __BibTex Key__, preceded by the __at-sign__ `@` (e.g.: `@VargasLlosa1975`).
	
	- __Tip__: the standard __Pandoc__ output will produce a _Name (Year)_ output for a simple `@BibTexKey` reference, and a _(Name Year)_ output for a `[@BibTexKey]` reference between square brackets; once you have started using __Pandoc__, try experimenting with these options:
	
		- `@VargasLlosa1975` will result in "Vargas Llosa (1975)";

		- `[@VargasLlosa1975]` will result in "(Vargas Llosa 1975)"; 

		- `[as in @VargasLlosa1975]` will result in "(as in Vargas Llosa 1975)";

		- `[@VargasLlosa1975 page 16]` will result in "(Vargas Llosa 1975, 16)".

5. To include an index of your references at the end of your paper, simply insert a `#References` or `##Bibliography` empty section; __Pandoc__ will compile one for you.

##4. Presenting your paper

1. Once you are done with your work, use __Pandoc__ for a quick conversion of your __.md__ file into the format of your choice (__.doc__, __.html__, __.docx__, __.pdf__). Install __Pandoc__ by following the instructions presented on its [web site](http://johnmacfarlane.net/pandoc/installing.html); the software is available for most operating systems.

2. Verify that you have correctly installed Pandoc by typing the command `pandoc --version` in your terminal; if you get information about the version currently installed, you are all set.

3. Prepare your __.md__ file by adding a __YAML__ block at the beginning; this small object will provide __Pandoc__ with the necessary information for the conversion. Here is an example of how it will look like:

	```
	title: Shakespeare's Sonnets and the Advent of Printing
	author: G. E. Saretto
	date: January 17, 2015
	bibliography: sonnets.bib
	```
	- __Tip__: the crucial part of this step is identifying the path to the `bibliography:` file; remember that it has to be located in __the same folder__ as the main __.md__ file - otherwise __Pandoc__ won't be able to find it.

4. Run __Pandoc__ by invoking it in the terminal; your command line will look like this: `pandoc -oS sonnets.odt --filter pandoc-citeproc sonnets.md`. Notice that the __output__ precedes the __input__ in the program's syntax, which is as follows:

	5. `pandoc` is simply the invocation of the program;
	
	6. the two combined flags `-o` and `-S` (resulting in `-oS`) tell __Pandoc__ to:
	
		- `-o` - write the __o__utput to the specified _file_ (the one that immediately follows), and in the format of our choice (__.doc__, __.pdf__, __.html__, etc.);
		
		- `-S` - operate __s__mart choices in determining the format of the layout, detecting typographical correspondences between the format of the input and that of the output;
	
	5. `sonnets.odt` is the __output__, with an extension corresponding to the format of my choice;
	
	6. `--filter pandoc-citeproc` asks __Pandoc__ to use one of its secondary implementations, a devoted _CiteProc_ program, in order to identify and match our references and produce a bibliography;
	
	7. `sonnets.md` is the __input__, the original file on which you have been working on.

		- __Tip__: __Pandoc__ requires an piece of software, a __LaTeX__ engine, in order to work; [MiKTeX](http://miktex.org/) is the standard option for Windows, [TeXLive](http://www.tug.org/texlive/) the one for Linux.

5. __Good job!__ The final file, a printable version of your paper featuring a clear layout and a complete bibliography, is  in your working folder, ready to be distributed.  Remember to provide a link to your __GitHub__ repository!