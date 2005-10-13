
size = scalable
context = apps

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =					\
	accessories-calculator.svg		\
	accessories-text-editor.svg		\
	evolution.svg				\
	help-browser.svg			\
	internet-group-chat.svg			\
	internet-mail.svg			\
	internet-news-reader.svg		\
	internet-web-browser.svg		\
	multimedia-volume-control.svg		\
	office-calendar.svg			\
	preferences-desktop-accessibility.svg	\
	preferences-desktop-font.svg		\
	preferences-desktop-screensaver.svg	\
	preferences-desktop-theme.svg		\
	preferences-desktop-wallpaper.svg	\
	preferences-system-session.svg		\
	preferences-system-windows.svg		\
	system-file-manager.svg			\
	system-installer.svg			\
	system-lock-screen.svg			\
	system-software-update.svg		\
	system-users.svg			\
	utilities-system-monitor.svg

EXTRA_DIST =					\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))

