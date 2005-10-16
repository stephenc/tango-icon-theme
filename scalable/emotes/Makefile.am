
size = scalable
context = emotes

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	face-happy.svg	\
	face-crying.svg	\
	face-grin.svg	\
	face-laughing.svg	\
	face-sad.svg	\
	face-shocked.svg

EXTRA_DIST =				\
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

