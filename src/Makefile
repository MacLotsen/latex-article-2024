OUTPUT_DIR ?= ../out
BIB_FILE = references.bib
BIB_TARGET = $(OUTPUT_DIR)/references.bib

DEMO_FILES = $(OUTPUT_DIR)/invoice-template.pdf $(OUTPUT_DIR)/invoice-001.pdf $(OUTPUT_DIR)/invoice-002.pdf
DEMO2_FILES = $(OUTPUT_DIR)/invoice2-template.pdf

DEPS = ./the-article.tex sections/conclusie.tex sections/discussie.tex sections/inleiding.tex sections/legacy-factuur.tex sections/uitvoering.tex sections/yaml-interfaces.tex

COPY = cp
ifeq ($(OS),Windows_NT)
	OUTPUT_DIR = ..\out
	BIB_TARGET = $(OUTPUT_DIR)\references.bib
	COPY = copy /y
endif

$(OUTPUT_DIR)/%.pdf: $(DEPS)
	latexmk -outdir=$(OUTPUT_DIR) -pdf -dvi- -interaction=nonstopmode -bibtex $*
	cd $(OUTPUT_DIR) && latexmk -c $*.aux

$(BIB_TARGET): $(BIB_FILE)
	$(COPY) $(BIB_FILE) $(BIB_TARGET)

$(DEMO_FILES):
	$(MAKE) -C demo all

$(DEMO2_FILES):
	$(MAKE) -C demo-splitted/grapefruit template

article: $(DEMO_FILES) $(DEMO2_FILES) $(BIB_TARGET) $(OUTPUT_DIR)/the-article.pdf

intro: $(OUTPUT_DIR)/the-author.pdf

topics: $(OUTPUT_DIR)/article-topics.pdf

all: article intro topics
