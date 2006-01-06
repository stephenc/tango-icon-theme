
size = scalable
context = devices

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =				\
	audio-card.svg			\
	audio-input-microphone.svg	\
	battery.svg			\
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
	media-floppy.svg		\
	multimedia-player.svg		\
	network-wired.svg		\
	network-wireless.svg		\
	printer.svg			\
	video-display.svg

EXTRA_DIST =				\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
if ENABLE_LARGE_BITMAPS
	for i in 32 48 64 72 96 128; do \
		pngdir="$(DESTDIR)$(themedir)/$${i}x$${i}/$(context)"; \
		$(mkinstalldirs) $$pngdir; \
		for icon in $(icons_DATA); do \
			$(top_builddir)/svg2png.sh $$i $$pngdir $$icon; \
		done; \
		(cd $(DESTDIR)$(themedir)/$${i}x$${i} && $(ICONMAP) -c $(context)); \
	done
endif

