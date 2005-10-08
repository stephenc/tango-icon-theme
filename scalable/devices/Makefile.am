
size = scalable
context = devices

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	audio-card.svg			\
	battery.svg					\
	camera-photo.svg		\
	camera-video.svg		\
	computer.svg			\
	drive-cdrom.svg			\
	drive-harddisk.svg		\
	drive-removable-media.svg	\
	input-gaming.svg		\
	input-keyboard.svg		\
	input-mouse.svg			\
	media-cdrom.svg			\
	network.svg					\
	network-wireless.svg	\
	printer.svg			\
	video-display.svg

EXTRA_DIST =				\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
