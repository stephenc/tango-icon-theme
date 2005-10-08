
size = 22x22
context = actions

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	address-book-new.png	\
	appointment-new.png	\
	contact-new.png		\
	document-new.png	\
	document-print.png	\
	document-template.png	\
	go-next.png		\
	go-jump.png		\
	go-previous.png		\
	system-log-out.png	\
	system-search.png	\
	view-refresh.png

EXTRA_DIST =				\
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
