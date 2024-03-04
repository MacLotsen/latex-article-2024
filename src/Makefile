OUTPUT_DIR ?= ../out
BIB_FILE = references.bib
BIB_TARGET = $(OUTPUT_DIR)/references.bib

DEMO_FILES = $(OUTPUT_DIR)/invoice-template.pdf $(OUTPUT_DIR)/invoice-001.pdf $(OUTPUT_DIR)/invoice-002.pdf

$(OUTPUT_DIR)/%.pdf:
	latexmk -outdir=$(OUTPUT_DIR) -pdf -dvi- -interaction=nonstopmode -bibtex $*
	cd $(OUTPUT_DIR) && latexmk -c $*.aux

$(BIB_TARGET): $(BIB_FILE)
	cp $(BIB_FILE) $(BIB_TARGET)

$(DEMO_FILES):
	$(MAKE) -C demo all

article: $(DEMO_FILES) $(BIB_TARGET) ../out/the-article.pdf

intro: ../out/the-author.pdf

topics: ../out/article-topics.pdf

all: article intro topics
