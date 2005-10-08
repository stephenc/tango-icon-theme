
size = scalable
context = categories

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	preferences-desktop.svg

EXTRA_DIST =				\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
