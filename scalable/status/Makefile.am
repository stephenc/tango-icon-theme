
size = scalable
context = status

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =			\
	battery-caution.svg	\
	dialog-information.svg	\
	image-loading.svg \
	image-missing.svg

EXTRA_DIST =			\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
