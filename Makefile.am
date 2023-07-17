bin_PROGRAMS = water

dist_man_MANS = water.1

dist_doc_DATA = \
	LICENSE \
	NEWS \
	README

water_SOURCES = \
	button.c \
	client.c \
	dragger.c \
	ewmh.c \
	frame.c \
	lib.c \
	list.h \
	main.c \
	mwm.c \
	root.c \
	water.h \
	deleven.xbm \
	delodd.xbm

if CONFIG_XFT
water_SOURCES+=xftfont.c
else
water_SOURCES+=x11font.c
endif

water_LDFLAGS = $(X_LIBS)
water_LDADD = $(xft_LIBS) $(X_PRE_LIBS) -lX11 $(X_EXTRA_LIBS)
