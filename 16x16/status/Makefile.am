
size = 16x16
context = status

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =			\
	battery-caution.png	\
	dialog-error.png	\
	dialog-information.png	\
	dialog-warning.png	\
	image-loading.png	\
	image-missing.png	\
	locked.png	\
	mail-attachment.png \
	unlocked.png

EXTRA_DIST =			\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
