
size = scalable
context = emotes

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	face-happy.svg	\
	face-crying.svg	\
	face-grin.svg	\
	face-laughing.svg	\
	face-sad.svg	\
	face-shocked.svg

EXTRA_DIST =				\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
