#!make

TEX=pdflatex #cslatex
NAME=thesis

all: $(NAME).pdf

# Vyroba PDF primo z DVI by byla prijemnejsi, ale vetsina verzi dvipdfm nici obrazky
# prace.pdf: prace.dvi
#	dvipdfm -o $@ -p a4 -r 600 $<

#prace.pdf: prace.ps
#	ps2pdf $< $@

#prace.ps: prace.dvi
#	dvips -o $@ -D600 -t a4 $<


# LaTeX je potreba spustit dvakrat, aby spravne spocital odkazy
$(NAME).pdf: $(NAME).tex text/*.tex
	$(TEX) $<
	$(TEX) $<

clean:
	rm -f *.{log,dvi,aux,toc,loa,lof,lot,out} $(NAME).ps $(NAME).pdf

distclean: clean
	find . -name "*~" -or -name "*.aux" -delete 
	rm *~
