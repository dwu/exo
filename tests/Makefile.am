
SUBDIRS =								\
	data

AM_CPPFLAGS =								\
	-I$(top_srcdir)							\
	-DG_LOG_DOMAIN=\"exo-tests\"

TESTS =									\
	test-exo-csource						\
	test-exo-noop							\
	test-exo-string

check_PROGRAMS =							\
	test-exo-csource						\
	test-exo-noop							\
	test-exo-string							\
	test-exo-icon-chooser-dialog					\
	test-exo-icon-chooser-dialog-gtk3					\
	test-exo-wrap-table

test_exo_csource_SOURCES =						\
	test-exo-csource.c						\
	test-exo-csource-data.c

test_exo_csource_CFLAGS =						\
	$(GLIB_CFLAGS)

test_exo_csource_LDADD =						\
	$(GLIB_LIBS)

test_exo_noop_SOURCES =							\
	test-exo-noop.c

test_exo_noop_CFLAGS =							\
	$(GTK_CFLAGS)							\
	$(LIBXFCE4UTIL_CFLAGS)

test_exo_noop_DEPENDENCIES =						\
	$(top_builddir)/exo/libexo-$(LIBEXO_VERSION_API).la

test_exo_noop_LDADD =							\
	$(GLIB_LIBS)							\
	$(top_builddir)/exo/libexo-$(LIBEXO_VERSION_API).la

test_exo_string_SOURCES =						\
	test-exo-string.c

test_exo_string_CFLAGS =						\
	$(GTK_CFLAGS)							\
	$(LIBXFCE4UTIL_CFLAGS)

test_exo_string_DEPENDENCIES =						\
	$(top_builddir)/exo/libexo-$(LIBEXO_VERSION_API).la

test_exo_string_LDADD =							\
	$(GLIB_LIBS)							\
	$(top_builddir)/exo/libexo-$(LIBEXO_VERSION_API).la

test_exo_icon_chooser_dialog_SOURCES =					\
	test-exo-icon-chooser-dialog.c

test_exo_icon_chooser_dialog_CFLAGS =					\
	$(GTK_CFLAGS)							\
	$(LIBXFCE4UTIL_CFLAGS)

test_exo_icon_chooser_dialog_DEPENDENCIES =				\
	$(top_builddir)/exo/libexo-$(LIBEXO_VERSION_API).la

test_exo_icon_chooser_dialog_LDADD =					\
	$(GTK_LIBS)							\
	$(top_builddir)/exo/libexo-$(LIBEXO_VERSION_API).la

test_exo_icon_chooser_dialog_gtk3_SOURCES =					\
	test-exo-icon-chooser-dialog.c

test_exo_icon_chooser_dialog_gtk3_CFLAGS =					\
	$(GTK3_CFLAGS)							\
	$(LIBXFCE4UTIL_CFLAGS)

test_exo_icon_chooser_dialog_gtk3_DEPENDENCIES =				\
	$(top_builddir)/exo/libexo-2.la

test_exo_icon_chooser_dialog_gtk3_LDADD =					\
	$(GTK3_LIBS)							\
	$(top_builddir)/exo/libexo-2.la

test_exo_wrap_table_SOURCES =						\
	test-exo-wrap-table.c

test_exo_wrap_table_CFLAGS =						\
	$(GTK_CFLAGS)							\
	$(LIBXFCE4UTIL_CFLAGS)

test_exo_wrap_table_DEPENDENCIES =					\
	$(top_builddir)/exo/libexo-$(LIBEXO_VERSION_API).la

test_exo_wrap_table_LDADD =						\
	$(GTK_LIBS)							\
	$(top_builddir)/exo/libexo-$(LIBEXO_VERSION_API).la

DISTCLEANFILES = test-exo-csource-data.c
BUILT_SOURCES = test-exo-csource-data.c

test-exo-csource-data.c: Makefile $(srcdir)/data/data.bin $(srcdir)/data/data.txt
	$(top_builddir)/exo-csource/exo-csource --extern --build-list data_bin $(srcdir)/data/data.bin data_txt $(srcdir)/data/data.txt > test-exo-csource-data.c

clean-local:
	rm -f *.core core core.*

# vi:set ts=8 sw=8 noet ai nocindent syntax=automake:
