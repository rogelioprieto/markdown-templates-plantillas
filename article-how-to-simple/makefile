all: pdf-notoc  view

pdf:
	pandoc -s \
	-V lang=es-mx \
	--toc --toc-dept=4 \
	--number-sections \
	-V documentclass=article \
	myarticle.md -o myarticle.pdf

pdf-notoc:
	pandoc -s \
	-V lang=es-mx \
	--number-sections \
	-V documentclass=article \
	myarticle.md -o myarticle.pdf
	
html:
	pandoc myarticle.md -V lang=spanish --toc --toc-depth=4  --self-contained -o myarticle.html

view:
	evince myarticle.pdf &
	#firefox alcance-cotizacion-muebles.html
