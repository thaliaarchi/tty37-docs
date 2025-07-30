PDFS = 574-301-100-iss1-7106 574-302-102-iss1-7105 574-302-300-iss1-7204 \
	574-320-101-iss2-7302 catalog_1969

.PHONY: all download figures

all: download figures

# $1: Input PDF stem
# $2: Extracted image number: ????.p[bg]m
# $3: ImageMagick transformations
# $4: Output PNG stem
define extract_figure
PDFS += $1
FIGURES += $4.png

$4.png: | pages/$1-$2
	magick pages/$1-$2 $3 -strip $$@

pages/$1-$2: | pages/$1.stamp
endef

# Crop page 7 to 2030x582+352+338 with 40px padding
$(eval $(call extract_figure,574-301-100-iss1-7106,0006.pbm,-rotate 90 -crop 2110x662+312+298,keyboard))
# Crop page 7 to 2136x1068+312+1604 with 100px padding
$(eval $(call extract_figure,574-301-100-iss1-7106,0006.pbm,-rotate 90 -crop 2336x1268+212+1504,control_panel))

download: $(PDFS:=.pdf)
figures: $(FIGURES)
	rm -rf pages

# brew install ocrmypdf
%.ocr.pdf: %.pdf
	ocrmypdf -l eng --redo-ocr $< $@

%.pdf:
	wget https://www.navy-radio.com/manuals/tty/m37/$@
catalog_1969.pdf:
	wget -O $@ https://archive.org/download/TNM_Model_37_terminal_product_catalog_-_Teletype__20170923_0036/TNM_Model_37_terminal_product_catalog_-_Teletype__20170923_0036.pdf

# TODO: Although the extract_figure targets use order-only prerequisites (pipe),
# since pages/ is deleted by figures, pdfimages is run every time.
pages/%.stamp: %.pdf
	@mkdir -p pages
	pdfimages $< pages/$*
	@touch $@

.PHONY: clean
clean:
	rm -rf $(FIGURES) pages
