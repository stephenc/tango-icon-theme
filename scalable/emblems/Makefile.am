
size = scalable
context = emblems

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	emblem-photos.svg

EXTRA_DIST =				\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
