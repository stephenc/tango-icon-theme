
size = 16x16
context = apps

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA =					\
	accessories-calculator.png		\
	accessories-text-editor.png		\
	evolution.png				\
	help-browser.png			\
	internet-group-chat.png			\
	internet-mail.png			\
	internet-news-reader.png		\
	internet-web-browser.png		\
	multimedia-volume-control.png		\
	office-calendar.png			\
	preferences-desktop-accessibility.png	\
	preferences-desktop-font.png		\
	preferences-desktop-screensaver.png	\
	preferences-desktop-theme.png		\
	preferences-desktop-wallpaper.png	\
	preferences-system-session.png		\
	preferences-system-windows.png		\
	system-file-manager.png			\
	system-installer.png			\
	system-lock-screen.png			\
	system-software-update.png		\
	system-users.png

EXTRA_DIST =					\
	$(icons_DATA)

install-data-local: install-iconsDATA
	(cd $(DESTDIR)$(themedir)/$(size) && $(ICONMAP) -c $(context))
