
size = scalable
context = actions

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =			\
	address-book-new.svg	\
	appointment-new.svg	\
	contact-new.svg		\
	document-new.svg	\
	document-print.svg	\
	document-template.svg	\
	go-jump.svg		\
	go-next.svg		\
	go-previous.svg		\
	system-log-out.svg	\
	system-search.svg	\
	system-shutdown.svg	\
	view-refresh.svg

EXTRA_DIST =			\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
