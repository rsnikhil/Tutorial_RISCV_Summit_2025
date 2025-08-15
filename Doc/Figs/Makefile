# This Makefile has a generic rule to convert an .svg file into a .png file using Inkscape

.PHONY: help
help:
	@echo "Available 'make' targets:"
	@echo "  <file>.png    generate '<file>.png' from '<file>.svg' using inkscape"
	@echo ""
	@echo "  all           $(ALL)"
	@echo "  help          show this help text"
	@echo "  clean         remove temporary intermediate files"
	@echo "  full_clean    restore directory to pristine state"

# ================================================================
# RULES

DIAGS_2025 = $(HOME)/Diagrams/2025

%.png: $(DIAGS_2025)/%.svg
	inkscape --export-filename=$@  --export-area-drawing  -d 300 -y 0.0 $<

# ================================================================

ALL_FIGS += RSN_2025-07-25.000.00_Tutorial_Plan.png
ALL_FIGS += RSN_2025-08-15.000.00_Tutorial_Resources.png

.PHONY: all
all: $(ALL_FIGS)

# ================================================================

.PHONY: clean
clean:
	rm -r -f *~

.PHONY: full_clean
full_clean: clean
	rm -r -f $(ALL_FIGS)
