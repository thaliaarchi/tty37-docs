MANUALS := 574-301-100-iss1-7106 574-302-102-iss1-7105 574-302-300-iss1-7204 \
	catalog_1969.ocr
PDF := $(patsubst %, %.pdf, $(MANUALS))
FIGURES := keyboard.png control_panel.png

.PHONY: docs
docs: $(PDF) $(FIGURES)

%.pdf:
	wget https://www.navy-radio.virhistory.com/manuals/tty/m37/$@

catalog_1969.pdf:
	wget -O $@ https://archive.org/download/TNM_Model_37_terminal_product_catalog_-_Teletype__20170923_0036/TNM_Model_37_terminal_product_catalog_-_Teletype__20170923_0036.pdf
# brew install ocrmypdf
catalog_1969.ocr.pdf: catalog_1969.pdf
	ocrmypdf -l eng --redo-ocr $< $@

# Extract the keyboard and control panel arrangement graphics from page 7 of
# 574-301-100. The keyboard arrangement graphic is duplicated on page 5 of
# 574-302-102, but with thinner lines and slightly askew.
.INTERMEDIATE: arrangements.pbm
arrangements.pbm: 574-301-100-iss1-7106.pdf
	pdfimages -f 7 -l 7 $< page
	mv page-0000.pbm arrangements.pbm

# Crop to 2030x582+352+338 with 40px padding
keyboard.png: CROP := 2110x662+312+298
# Crop to 2136x1068+312+1604 with 100px padding
control_panel.png: CROP := 2336x1268+212+1504

# Rotate, crop, and strip EXIF metadata
%.png: arrangements.pbm
	magick $< -rotate 90 -crop $(CROP) $@
	mogrify -strip $@

.PHONY: clean
clean:
	rm -rf $(FIGURES) arrangements.pbm
