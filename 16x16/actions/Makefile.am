
size = 16x16
context = actions

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =			\
	address-book-new.png	\
	appointment-new.png	\
	bookmark-new.png	\
	contact-new.png		\
	document-new.png	\
	document-print.png	\
	edit-paste.png		\
	go-down.png	\
	go-home.png		\
	go-jump.png		\
	go-next.png		\
	go-previous.png		\
	go-up.png	\
	process-stop.png	\
	system-log-out.png	\
	system-search.png	\
	system-shutdown.png	\
	view-refresh.png

EXTRA_DIST =			\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
