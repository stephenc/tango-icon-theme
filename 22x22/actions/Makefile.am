
size = 22x22
context = actions

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =			\
	address-book-new.png	\
	appointment-new.png	\
	bookmark-new.png	\
	contact-new.png		\
	document-new.png	\
	document-open.png	\
	document-print.png	\
	document-print-preview.png	\
	document-properties.png	\
	document-save.png	\
	edit-copy.png		\
	edit-cut.png	\
	edit-paste.png		\
	edit-redo.png	\
	edit-undo.png	\
	format-indent-less.png	\
	format-indent-more.png	\
	format-justify-center.png	\
	format-justify-fill.png	\
	format-justify-left.png	\
	format-justify-right.png	\
	go-bottom.png	\
	go-down.png	\
	go-first.png	\
	go-home.png		\
	go-jump.png		\
	go-last.png	\
	go-next.png		\
	go-previous.png		\
	go-top.png	\
	go-up.png	\
	help-contents.png	\
	process-stop.png	\
	system-log-out.png	\
	system-search.png	\
	system-shutdown.png	\
	tab-new.png	\
	view-refresh.png

EXTRA_DIST =			\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
if ENABLE_ICON_FRAMING
	$(mkinstalldirs) $(DESTDIR)$(themedir)/24x24/$(context)
	(cd $(DESTDIR)$(themedir) && \
	for icon in $(icons_DATA); do \
		$(CONVERT) $(size)/$(context)/$$icon 24x24/$(context)/$$icon; \
	done)
	(cd $(DESTDIR)$(themedir)/24x24 && $(ICONMAP) -c $(context))
endif

uninstall-local:
	rm -rf $(themedir)/24x24/$(context)
