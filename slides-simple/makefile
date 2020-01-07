all: easy

easy: mypresentation.md
	pandoc -t beamer --toc --toc-depth=3 \
	-H packages/simple-theme-uas-blue.tex \
	mypresentation.md -o mypresentation.pdf


view: mypresentation.pdf
	evince mypresentation.pdf &


