DISTCHECK_CONFIGURE_FLAGS = --disable-icon-framing

SUBDIRS = 16x16 22x22 scalable po

THEME_IN_FILES = index.theme.in

@INTLTOOL_THEME_RULE@

noinst_SCRIPTS = svg2png.sh

%.sh: %.sh.in
	sed -e "s|\@SVGCONVERT\@|$(SVGCONVERT)|g" < $< > $@
	chmod +x $@

theme_DATA = index.theme

EXTRA_DIST=				\
	$(THEME_IN_FILES)		\
	svg2png.sh.in			\
	intltool-update.in 		\
	intltool-merge.in 		\
	intltool-extract.in

# we don't want to install mo files, all translations are already stored
# in theme files
install-data-local:
	$(MAKE) -C po uninstall
	if [ -h $(DESTDIR)$(themedir) ]; then \
		rm -f $(DESTDIR)$(themedir); \
	fi
	if [ -d $(DESTDIR)$(themedir) ]; then \
		touch $(DESTDIR)$(themedir); \
	fi

CLEANFILES = 				\
	index.theme			\
	svg2png.sh

DISTCLEANFILES = 			\
	intltool-extract		\
	intltool-merge			\
	intltool-update

MAINTAINERCLEANFILES =			\
	Makefile.in			\
	aclocal.m4			\
	configure			\
	install-sh			\
	intltool-extract.in		\
	intltool-merge.in		\
	intltool-update.in		\
	missing				\
	mkinstalldirs

