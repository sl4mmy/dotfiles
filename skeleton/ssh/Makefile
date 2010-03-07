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

install: ${HOME}/.ssh/ ${HOME}/.ssh/id_dsa.pub

clean: clean-public-key

force: clean install

${HOME}/.ssh/:
	mkdir ${HOME}/.ssh
	chmod go-rwx ${HOME}/.ssh

# Copy id_dsa.pub, instead of linking, because OpenSSH is very strict about
# that sort of thing
${HOME}/.ssh/id_dsa.pub:
	cp id_dsa.pub ${HOME}/.ssh/id_dsa.pub

clean-public-key:
	-rm ${HOME}/.ssh/id_dsa.pub
