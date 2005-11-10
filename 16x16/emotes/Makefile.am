
size = 16x16
context = emotes

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	face-angel.png	\
	face-crying.png	\
	face-grin.png	\
	face-laughing.png	\
	face-sad.png	\
	face-shocked.png	\
	face-smile.png	\
	face-wink.png

EXTRA_DIST =				\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
