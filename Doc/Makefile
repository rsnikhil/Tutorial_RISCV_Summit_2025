.PHONY: help
help:
	@echo "Targets:"
	@echo "  all    Uses asciidoctor to converts .adoc documents into .html documents"

all: Resources.html

%.html: %.adoc
	asciidoctor $<
