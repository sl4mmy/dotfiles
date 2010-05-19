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

install: ${HOME}/.zprofile ${HOME}/.zshenv ${HOME}/.zshrc

clean: clean-zprofile clean-zshenv clean-zshrc

force: clean install

${HOME}/.zprofile:
	ln -s ${CURDIR}/zprofile ${HOME}/.zprofile

clean-zprofile:
	-rm ${HOME}/.zprofile

${HOME}/.zshenv:
	ln -s ${CURDIR}/zshenv ${HOME}/.zshenv

clean-zshenv:
	-rm ${HOME}/.zshenv

${HOME}/.zshrc:
	ln -s ${CURDIR}/zshrc ${HOME}/.zshrc

clean-zshrc:
	-rm ${HOME}/.zshrc

.PHONY: install clean force clean-zprofile clean-zshenv clean-zshrc
