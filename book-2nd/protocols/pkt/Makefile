#
# OB additions
# Automatic conversion of images
#
PKT2SVG= ../../../book/util/packet2svg.py
SVG2PNG= ../../../book/util/convertpkt.sh

SVGFILES := $(patsubst %.pkt,%.svg,$(wildcard *.pkt))
IMAGES := $(patsubst %.pkt,%.png,$(wildcard *.pkt))

%.svg: %.pkt
	$(PKT2SVG) $<

%.png: %.svg
	@echo converting $<
	$(SVG2PNG) $<

images: ${SVGFILES} ${IMAGES}
	@echo "All images converted"
