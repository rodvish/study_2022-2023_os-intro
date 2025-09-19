all: presentation.pdf presentation.html

presentation.pdf: presentation.md
	pandoc presentation.md -o presentation.pdf \
	--resource-path=.:image \
	-t beamer \
	--pdf-engine=xelatex \
	-V mainfont="Liberation Sans" \
	-V sansfont="Liberation Sans" \
	-V monofont="Liberation Mono" \
	--slide-level=2

presentation.html: presentation.md
	pandoc presentation.md -o presentation.html \
	--resource-path=.:image \
	-t revealjs \
	--self-contained

clean:
	rm -f presentation.pdf presentation.html

.PHONY: all clean
