SUBDIRS = 16x16 22x22 24x24 32x32 48x48 scalable

gtk_update_icon_cache = gtk-update-icon-cache -f -t $(datadir)/icons/hicolor

update-icon-cache:
	@-if test -z "$(DESTDIR)"; then \
		echo "Updating Gtk icon cache."; \
		$(gtk_update_icon_cache); \
	else \
		echo "*** Icon cache not updated.  After install, run this:"; \
		echo "***   $(gtk_update_icon_cache)"; \
	fi

install-data-hook: update-icon-cache
uninstall-hook: update-icon-cache

clean-local :
	rm -f *~
