
size = 16x16
context = mimetypes

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =					\
	application-certificate.png		\
	application-x-executable.png		\
	audio-x-generic.png			\
	image-x-generic.png			\
	package-x-generic.png			\
	text-html.png				\
	text-x-generic.png			\
	text-x-generic-template.png			\
	text-x-script.png			\
	video-x-generic.png			\
	x-directory-desktop.png			\
	x-directory-normal-drag-accept.png	\
	x-directory-normal-home.png		\
	x-directory-normal-open.png		\
	x-directory-normal-visiting.png		\
	x-directory-normal.png			\
	x-directory-remote.png			\
	x-directory-remote-server.png		\
	x-directory-remote-workgroup.png	\
	x-directory-trash-full.png		\
	x-directory-trash.png			\
	x-office-address-book.png		\
	x-office-spreadsheet.png

EXTRA_DIST =					\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
