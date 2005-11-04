
size = 16x16
context = emblems

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	emblem-favorites.png	\
	emblem-photos.png	\
	emblem-system.png

EXTRA_DIST =				\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
