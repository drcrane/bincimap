# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.

# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Street #330, Boston, MA 02111-1307,
# USA.

#--------------------------------------------------------------------------
EXTRA_DIST=run run-ssl

#--------------------------------------------------------------------------
install-exec-hook:
	$(mkinstalldirs) $(DESTDIR)$(localstatedir)/service/bincimap/log
	@if [ ! -e $(DESTDIR)$(localstatedir)/service/bincimap/log/run ]; then $(INSTALL_SCRIPT) -m 0755 $(srcdir)/run $(DESTDIR)$(localstatedir)/service/bincimap/log/run;  else $(INSTALL_SCRIPT) -m 0755 $(srcdir)/run $(DESTDIR)$(localstatedir)/service/bincimap/log/run.new; echo "- New service/bincimap/run file saved as $(DESTDIR)$(localstatedir)/service/bincimap/log/run.new" >> $(srcdir)/../../install.log; fi
	$(mkinstalldirs) $(DESTDIR)$(localstatedir)/service/bincimaps/log
	@if [ ! -e $(DESTDIR)$(localstatedir)/service/bincimaps/log/run ]; then $(INSTALL_SCRIPT) -m 0755 $(srcdir)/run-ssl $(DESTDIR)$(localstatedir)/service/bincimaps/log/run;  else $(INSTALL_SCRIPT) -m 0755 $(srcdir)/run-ssl $(DESTDIR)$(localstatedir)/service/bincimaps/log/run.new; echo "- New service/bincimaps/run file saved as $(DESTDIR)$(localstatedir)/service/bincimaps/log/run.new" >> $(srcdir)/../../install.log; fi;

#--------------------------------------------------------------------------
uninstall-hook:
	rm $(DESTDIR)$(localstatedir)/service/bincimap/log/run
	rm $(DESTDIR)$(localstatedir)/service/bincimaps/log/run
