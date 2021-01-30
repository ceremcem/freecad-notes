all:
	# NOTICE: Make sure that Pandoc version is >= 2.11
	pandoc -f gfm -t html5 -o index.html README.md --css=gh-pandoc.css -s
	sensible-browser index.html

upload:
	surge .
