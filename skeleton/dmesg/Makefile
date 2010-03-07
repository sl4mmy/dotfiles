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

install: ${HOME}/dmesg ${HOME}/dmesgs/ ${HOME}/dmesgs/.machine ${HOME}/sensors/

clean: clean-dmesg clean-machine clean-dmesgs clean-sensors

force: clean install

${HOME}/dmesg:
	ln -s ${.CURDIR}/script ${HOME}/dmesg

clean-dmesg:
	-rm ${HOME}/dmesg

${HOME}/dmesgs/:
	mkdir ${HOME}/dmesgs

clean-dmesgs:
	-rm -rf ${HOME}/dmesgs

${HOME}/dmesgs/.machine: ${HOME}/dmesgs/
	ln -s ${.CURDIR}/machine ${HOME}/dmesgs/.machine

clean-machine:
	-rm ${HOME}/dmesgs/.machine

${HOME}/sensors/:
	mkdir ${HOME}/sensors

clean-sensors:
	-rm -rf ${HOME}/sensors
