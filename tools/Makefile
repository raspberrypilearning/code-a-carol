SHELL=/bin/bash

# This will probably need changing on your system:
MUSESCORE=/opt/MuseScore-3.0.5-x86_64.AppImage

SRC_STEM=Twelve-days-fragments

all: introduction.png five-gold-rings.png four-three-two.png item.png partridge.png

%.pdf: %.mscz
	$(MUSESCORE) -o $@ $<

burst.witness: $(SRC_STEM).pdf
	@rm -f burst.tmp
	@touch burst.tmp
	pdftk $(SRC_STEM).pdf burst output p%d.pdf
	@mv -f burst.tmp burst.witness

p1.pdf p2.pdf p3.pdf p4.pdf p5.pdf: burst.witness

# The resolution here was chosen carefully to achieve a width of 800px
# for the widest images, including the padding which is done below.
#
p%.png: p%.pdf
	gs -sDEVICE=pngalpha -r152.875 -o tmp-$@ $<
	convert tmp-$@ -background '#FFFFFF' -flatten $@

cropped-p%.png: p%.png
	pngtopnm $< \
	  | pnmcrop -white \
	  | pnmpad -white -left 8 -right 8 -top 8 -bottom 8 \
	  | pnmtopng \
	> $@

introduction.png: cropped-p1.png
	cp $< $@

five-gold-rings.png: cropped-p2.png
	cp $< $@

four-three-two.png: cropped-p3.png
	cp $< $@

item.png: cropped-p4.png
	cp $< $@

partridge.png: cropped-p5.png
	cp $< $@

clean:
	rm -f p{1,2,3,4,5}.{png,pdf}
	rm -f tmp-p{1,2,3,4,5}.png
	rm -f cropped-p{1,2,3,4,5}.png
	rm -f burst.witness doc_data.txt
	rm -f introduction.png five-gold-rings.png four-three-two.png item.png partridge.png

install:
	cp --target-directory=../en/images \
		introduction.png five-gold-rings.png four-three-two.png item.png partridge.png
