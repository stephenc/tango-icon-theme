
size = scalable
context = categories

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	applications-accessories.svg	\
	applications-development.svg	\
	applications-games.svg	\
	applications-graphics.svg	\
	applications-internet.svg	\
	applications-multimedia.svg	\
	applications-office.svg	\
	applications-other.svg	\
	applications-system.svg	\
	preferences-desktop.svg	\
	preferences-desktop-peripherals.svg	\
	preferences-system.svg

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

