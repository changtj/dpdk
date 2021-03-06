#   BSD LICENSE
#
#   Copyright(c) 2016 Cavium, Inc. All rights reserved.
#
#   Redistribution and use in source and binary forms, with or without
#   modification, are permitted provided that the following conditions
#   are met:
#
#     * Redistributions of source code must retain the above copyright
#       notice, this list of conditions and the following disclaimer.
#     * Redistributions in binary form must reproduce the above copyright
#       notice, this list of conditions and the following disclaimer in
#       the documentation and/or other materials provided with the
#       distribution.
#     * Neither the name of Cavium, Inc nor the names of its
#       contributors may be used to endorse or promote products derived
#       from this software without specific prior written permission.
#
#   THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
#   "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
#   LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
#   A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
#   OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
#   SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
#   LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
#   DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
#   THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
#   (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
#   OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

include $(RTE_SDK)/mk/rte.vars.mk

# library name
LIB = librte_eventdev.a

# library version
LIBABIVER := 3

# build flags
CFLAGS += -O3
CFLAGS += $(WERROR_FLAGS)
LDLIBS += -lrte_eal -lrte_ring -lrte_ethdev -lrte_hash
LDLIBS += -lrte_cryptodev

# library source files
SRCS-y += rte_eventdev.c
SRCS-y += rte_event_ring.c
SRCS-y += rte_event_eth_rx_adapter.c
SRCS-y += rte_event_crypto_adapter.c

# export include files
SYMLINK-y-include += rte_eventdev.h
SYMLINK-y-include += rte_eventdev_pmd.h
SYMLINK-y-include += rte_eventdev_pmd_pci.h
SYMLINK-y-include += rte_eventdev_pmd_vdev.h
SYMLINK-y-include += rte_event_ring.h
SYMLINK-y-include += rte_event_eth_rx_adapter.h
SYMLINK-y-include += rte_event_crypto_adapter.h

# versioning export map
EXPORT_MAP := rte_eventdev_version.map

include $(RTE_SDK)/mk/rte.lib.mk
