
size = 16x16
context = categories

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	applications-development.png	\
	applications-games.png	\
	preferences-desktop.png

EXTRA_DIST =				\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
