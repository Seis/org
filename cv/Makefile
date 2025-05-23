OUTPUT_DIR = ../static
SRC = cv.tex
OUT = $(SRC:.tex=.pdf)

cv: $(OUT)

publ: JOB = publ
publ: $(OUT)

%.pdf: %.tex
	latexmk -outdir=$(OUTPUT_DIR) -interaction=nonstopmode -jobname=$(JOB) \
		-shell-escape -pdf -use-make -cd $<

clean:
	latexmk -outdir=$(OUTPUT_DIR) -cd -C -jobname=cv
	latexmk -outdir=$(OUTPUT_DIR) -cd -C -jobname=publ
	$(RM) $(OUTPUT_DIR)/*.bbl
