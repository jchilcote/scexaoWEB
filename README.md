# SCExAO public Webpage content

## Build local copy of website

To build on local machine (first time):

	git clone https://github.com/scexao-org/scexaoWEB
	cd scripts
	gcc makeweb.c -o makeweb
	cd ..
	./scripts/makeweb

To synchronize content (pull latest changes):

	git pull
	./scripts/makeweb

## Modifying the webpage content

To change content, edit files content.html. Do not change files indexm.html, as they are automatically generated by makeweb.

## Creating a new sub-page

- Create a .web directory, following this convention: 123name.web. The number is used to pick the order in which the page will appear in the menu.
- Inside the .web directory, create a title.txt file containing the title that should appear in the menu. Keep it short, and a single line.
- Place the html content in file content.html

To include the new page in the repo, remember to run :

	git add <.web directory>
	git commit -am 'new page'
	git push

## Deployment on Subaru website

Go to SCExAO website directory, then:

	cd scexaoWEB
	git pull
	./scripts/makeweb


