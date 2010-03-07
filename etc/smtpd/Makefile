# Copyright (c) 2010, Kent R. Spillner <kspillner@acm.org>
#
# Permission to use, copy, modify, and distribute this software for any
# purpose with or without fee is hereby granted, provided that the above
# copyright notice and this permission notice appear in all copies.
#
# THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
# WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
# MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
# ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
# WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
# ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
# OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

install-system: /etc/mailer.conf /etc/mail/smtpd.conf

destroy-system: destroy-mailer.conf destroy-smtpd.conf

/etc/mailer.conf:
	sudo cp mailer.conf /etc/mailer.conf

destroy-mailer.conf:
	-sudo rm /etc/mailer.conf

/etc/mail/smtpd.conf:
	sudo cp smtpd.conf /etc/mail/smtpd.conf

destroy-smtpd.conf:
	-sudo rm /etc/mail/smtpd.conf
