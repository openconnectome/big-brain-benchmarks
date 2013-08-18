LATEX = pdflatex
SPELL = aspell
TEX = big-brain-benchmarks
BIBTEX = bibtex

default: $(TEX).tex 
	$(LATEX) $(TEX); $(BIBTEX) $(TEX); $(LATEX) $(TEX); $(LATEX) $(TEX);
	$(RM) -f *.aux *.blg *.dvi *.log *.toc *.lof *.lot *.cb *.ps *.brf *.out
	open $(TEX).pdf &




view: $(TEX).tex 
	$(LATEX) $(TEX); $(BIBTEX) $(TEX); $(LATEX) $(TEX); $(LATEX) $(TEX)
	open $(TEX).pdf &

clean:
	$(RM) -f *.aux *.blg *.dvi *.log *.toc *.lof *.lot *.cb *.bbl $(TEX).ps $(TEX).pdf *~

check:
	@echo "Passing the check will cause make to report Error 1."
	$(LATEX) $(TEX)  | grep -i undefined
