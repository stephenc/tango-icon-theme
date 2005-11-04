
size = scalable
context = actions

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =			\
	address-book-new.svg	\
	appointment-new.svg	\
	bookmark-new.svg	\
	contact-new.svg		\
	document-new.svg	\
	document-open.svg	\
	document-print.svg	\
	document-properties.svg	\
	document-save.svg	\
	edit-copy.svg		\
	edit-cut.svg	\
	edit-paste.svg		\
	edit-redo.svg	\
	edit-undo.svg	\
	format-indent-less.svg	\
	format-indent-more.svg	\
	format-justify-center.svg	\
	format-justify-fill.svg	\
	format-justify-left.svg	\
	format-justify-right.svg	\
	go-bottom.svg	\
	go-down.svg	\
	go-first.svg	\
	go-home.svg		\
	go-jump.svg		\
	go-last.svg	\
	go-next.svg		\
	go-previous.svg		\
	go-top.svg	\
	go-up.svg	\
	help-contents.svg	\
	process-stop.svg	\
	system-log-out.svg	\
	system-search.svg	\
	system-shutdown.svg	\
	tab-new.svg	\
	view-refresh.svg

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
