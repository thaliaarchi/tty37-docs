PDFS = 574-301-100-iss1-7106 574-302-102-iss1-7105 574-302-300-iss1-7204 \
	574-320-101-iss2-7302 catalog_1969

.PHONY: all
all: download figures

# $1: Input PDF stem
# $2: Extracted image number: ????.p[bg]m
# $3: ImageMagick transformations
# $4: Crop
# $5: Border
# $6: Output PNG stem
define extract_figure
PDFS += $1
FIGURES += $1/$6.png

$1/$6.png: $1.pdf
	@if [ ! -f pages/$1-$2 ]; then \
		mkdir -p pages && \
		echo pdfimages $1.pdf pages/$1 && \
		pdfimages $1.pdf pages/$1; \
	fi
	@mkdir -p $1
	magick pages/$1-$2 $3 -crop $4 -trim -bordercolor white -border $5 -strip $$@
endef

$(eval $(call extract_figure,574-301-100-iss1-7106,0006.pbm,-rotate 90,2046x594+344+332,40,keyboard_layout))
$(eval $(call extract_figure,574-301-100-iss1-7106,0006.pbm,-rotate 90,2166x1092+296+1584,100,control_panel))

$(eval $(call extract_figure,574-320-101-iss2-7302,0088.pbm,-rotate 90,1714x904+533+268,80,visual_aid_overlay))

# Crop to 671x42+140+147 padded by 20
$(eval $(call extract_figure,chemical_teletype_1973,0001.pgm,-normalize,711x82+120+127,0,basic_symbols))
# Crop to 437x404+279+411 padded by 35,75,90,75
$(eval $(call extract_figure,chemical_teletype_1973,0001.pgm,-normalize,587x529+204+376,0,typebox_locations))
$(eval $(call extract_figure,chemical_teletype_1973,0001.pgm,,1184x967+232+1119,0,typebox))
$(eval $(call extract_figure,chemical_teletype_1973,0002.pgm,,656x830+25+154,0,typebox_pressed))
# Crop to 50x45+862+495 padded by 5
$(eval $(call extract_figure,chemical_teletype_1973,0002.pgm,-normalize,60x55+857+490,0,structure_1))
# Crop to 45x50+862+665 padded by 6
$(eval $(call extract_figure,chemical_teletype_1973,0002.pgm,-normalize,55x60+857+660,0,structure_2))
# Crop to 162x57+803+861 padded by 6
$(eval $(call extract_figure,chemical_teletype_1973,0002.pgm,-normalize,172x67+798+856,0,structure_3))
$(eval $(call extract_figure,chemical_teletype_1973,0002.pgm,,1380x965+24+1119,0,keyboard_with_overlay))
$(eval $(call extract_figure,chemical_teletype_1973,0003.pbm,-negate,1686x772+494+236,50,keyboard_layout))

.PHONY: download figures
download: $(PDFS:=.pdf)
figures: $(FIGURES)
	@rm -rf pages

# brew install ocrmypdf
%.ocr.pdf: %.pdf
	ocrmypdf -l eng --redo-ocr $< $@

%.pdf:
	wget https://www.navy-radio.com/manuals/tty/m37/$@
catalog_1969.pdf:
	wget -O $@ https://archive.org/download/TNM_Model_37_terminal_product_catalog_-_Teletype__20170923_0036/TNM_Model_37_terminal_product_catalog_-_Teletype__20170923_0036.pdf
chemical_teletype_1973.pdf:
	@echo 'Download chemical_teletype_1973.pdf from' >&2
	@echo 'https://pubs.acs.org/doi/abs/10.1021/c160049a003' >&2
	@echo '       or https://sci-hub.st/10.1021/c160049a003' >&2
	@exit 1

.PHONY: clean
clean:
	rm -rf $(FIGURES) pages
