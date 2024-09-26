all: compile
	sensible-browser index.html

compile:
	# NOTICE: Make sure that Pandoc version is >= 2.11
	pandoc -f markdown -w raw_attribute \
		-t html5 -o index.html README.md --css=gh-pandoc.css -s --metadata title=README

upload:
	surge .
