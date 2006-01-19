
size = scalable
context = emotes

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =			\
	face-angel.svg		\
	face-crying.svg		\
	face-devil-grin.svg	\
	face-glasses.svg	\
	face-grin.svg		\
	face-kiss.svg		\
	face-plain.svg		\
	face-sad.svg		\
	face-smile.svg		\
	face-smile-big.svg	\
	face-surprise.svg	\
	face-wink.svg

EXTRA_DIST =			\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
if ENABLE_LARGE_BITMAPS
	for i in 32 48 64 72 96 128; do \
		pngdir="$(DESTDIR)$(themedir)/$${i}x$${i}/$(context)"; \
		$(mkinstalldirs) $$pngdir; \
		for icon in $(icons_DATA); do \
			$(top_builddir)/svg2png.sh $$i $$pngdir $$icon; \
		done; \
		(cd $(DESTDIR)$(themedir)/$${i}x$${i} && $(ICONMAP) -c $(context)); \
	done
endif

