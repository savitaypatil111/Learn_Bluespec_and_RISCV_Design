FIGS += RSN_2025-09-01.002.00_Fig_Goals.png
FIGS += RSN_2025-10-13.000.00_Learn_Chapter_Roadmap.png

.PHONY: help
help:
	@echo "Targets:"
	@echo "  png    Produces .png files for all .svg files"

.PHONY: png
png: $(FIGS)

%.png: %.svg
	inkscape --export-filename=$@  --export-area-drawing  -d 300 -y 0.0 $<

DIAGRAMS_2025 = $(HOME)/Diagrams/2025

RSN_%.png: $(DIAGRAMS_2025)/RSN_%.svg
	inkscape --export-filename=$@  --export-area-drawing  -d 300 -y 0.0 $<
# ================================================================

.PHONY: clean
clean:
	rm -r -f  *~

.PHONY: full_clean
full_clean: clean
	rm -r -f  $(FIGS)
