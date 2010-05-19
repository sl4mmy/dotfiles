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

install: ${HOME}/build_kernel ${HOME}/build_userland ${HOME}/build_xenocara ${HOME}/kernel/

clean: clean-kernel clean-userland clean-xenocara clean-kernel-dir

force: clean install

${HOME}/build_kernel:
	ln -s ${CURDIR}/kernel ${HOME}/build_kernel

clean-kernel:
	-rm ${HOME}/build_kernel

${HOME}/build_userland:
	ln -s ${CURDIR}/userland ${HOME}/build_userland

clean-userland:
	-rm ${HOME}/build_userland

${HOME}/build_xenocara:
	ln -s ${CURDIR}/xenocara ${HOME}/build_xenocara

clean-xenocara:
	-rm ${HOME}/build_xenocara

${HOME}/kernel/:
	mkdir ${HOME}/kernel

clean-kernel-dir:
	-rm -rf ${HOME}/kernel

.PHONY: install clean force clean-kernel-dir clean-kernel clean-userland clean-xenocara
