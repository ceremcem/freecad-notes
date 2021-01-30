all:
	#bash -c "[[ $(pandoc -v | head -n1 | cut -d' ' -f2)" =~ 2\.11\..+ ]]" # check pandoc version
	pandoc -f gfm -t html5 -o index.html README.md --css=gh-pandoc.css -s
	sensible-browser index.html
