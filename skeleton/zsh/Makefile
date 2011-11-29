# Copyright (c) 2010, 2011, Kent R. Spillner <kspillner@acm.org>
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

install: ${HOME}/.zlogin ${HOME}/.zlogin.zwc ${HOME}/.zlogout ${HOME}/.zlogout.zwc ${HOME}/.zprofile ${HOME}/.zprofile.zwc ${HOME}/.zshenv ${HOME}/.zshenv.zwc ${HOME}/.zshrc ${HOME}/.zshrc.zwc

clean: clean-zlogin clean-zlogout clean-zprofile clean-zshenv clean-zshrc

force: clean install

${HOME}/.%:
	ln -fs ${CURDIR}/$(patsubst ${HOME}/.%,%,$@) $@

${HOME}/.zlogin.zwc: zlogin.zwc

zlogin.zwc: zlogin
	zsh -c "zcompile $<"

clean-zlogin:
	-rm ${HOME}/.zlogin ${HOME}/.zlogin.zwc
	-rm -f zlogin.zwc

${HOME}/.zlogout.zwc: zlogout.zwc

zlogout.zwc: zlogout
	zsh -c "zcompile $<"

clean-zlogout:
	-rm ${HOME}/.zlogout ${HOME}/.zlogout.zwc
	-rm -f zlogout.zwc

${HOME}/.zprofile.zwc: zprofile.zwc

zprofile.zwc: zprofile
	zsh -c "zcompile $<"

clean-zprofile:
	-rm ${HOME}/.zprofile ${HOME}/.zprofile.zwc
	-rm -f zprofile.zwc

${HOME}/.zshenv.zwc: zshenv.zwc

zshenv.zwc: zshenv
	zsh -c "zcompile $<"

clean-zshenv:
	-rm ${HOME}/.zshenv ${HOME}/.zshenv.zwc
	-rm -f zshenv.zwc

${HOME}/.zshrc.zwc: zshrc.zwc

zshrc.zwc: zshrc
	zsh -c "zcompile $<"

clean-zshrc:
	-rm ${HOME}/.zshrc ${HOME}/.zshrc.zwc
	-rm -f zshrc.zwc

.PHONY: install clean force clean-zlogin clean-zlogout clean-zprofile clean-zshenv clean-zshrc
