
size = scalable
context = mimetypes

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =					\
	application-certificate.svg		\
	application-x-executable.svg		\
	audio-x-generic.svg			\
	image-x-generic.svg			\
	package-x-generic.svg			\
	text-html.svg				\
	text-x-generic.svg			\
	text-x-generic-template.svg			\
	text-x-script.svg			\
	video-x-generic.svg			\
	x-directory-desktop.svg			\
	x-directory-normal-drag-accept.icon	\
	x-directory-normal-drag-accept.svg	\
	x-directory-normal-home.svg		\
	x-directory-normal-visiting.icon	\
	x-directory-normal-visiting.svg		\
	x-directory-normal.icon			\
	x-directory-normal.svg			\
	x-directory-remote.svg			\
	x-directory-remote-server.svg		\
	x-directory-remote-workgroup.svg	\
	x-directory-trash-full.svg		\
	x-directory-trash.svg			\
	x-office-address-book.svg		\
	x-office-spreadsheet.svg

EXTRA_DIST =					\
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

