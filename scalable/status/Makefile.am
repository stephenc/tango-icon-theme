
size = scalable
context = status

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	battery-caution.svg		\
	dialog-error.svg		\
	dialog-information.svg		\
	dialog-warning.svg		\
	folder-drag-accept.icon		\
	folder-drag-accept.svg		\
	folder-open.svg			\
	folder-visiting.icon		\
	folder-visiting.svg		\
	image-loading.svg		\
	image-missing.svg		\
	mail-attachment.svg		\
	network-wireless-encrypted.svg	\
	user-trash-full.svg

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

