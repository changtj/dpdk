#   BSD LICENSE
#
#   Copyright(c) 2010-2015 Intel Corporation. All rights reserved.
#   All rights reserved.
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
#     * Neither the name of Intel Corporation nor the names of its
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

# set in mk/toolchain/xxx/rte.toolchain-compat.mk
ifeq ($(CONFIG_RTE_LIBRTE_THUNDERX_NICVF_PMD),d)
        $(warning thunderx pmd is not supported by old compilers)
endif

DIRS-$(CONFIG_RTE_LIBRTE_PMD_AF_PACKET) += af_packet
DIRS-$(CONFIG_RTE_LIBRTE_ARK_PMD) += ark
DIRS-$(CONFIG_RTE_LIBRTE_AVP_PMD) += avp
DIRS-$(CONFIG_RTE_LIBRTE_BNX2X_PMD) += bnx2x
DIRS-$(CONFIG_RTE_LIBRTE_PMD_BOND) += bonding
DIRS-$(CONFIG_RTE_LIBRTE_CXGBE_PMD) += cxgbe
ifeq ($(CONFIG_RTE_LIBRTE_DPAA_BUS),y)
DIRS-$(CONFIG_RTE_LIBRTE_DPAA_PMD) += dpaa
endif
ifeq ($(CONFIG_RTE_EAL_VFIO)$(CONFIG_RTE_LIBRTE_FSLMC_BUS),yy)
DIRS-$(CONFIG_RTE_LIBRTE_DPAA2_PMD) += dpaa2
endif
DIRS-$(CONFIG_RTE_LIBRTE_E1000_PMD) += e1000
DIRS-$(CONFIG_RTE_LIBRTE_ENA_PMD) += ena
DIRS-$(CONFIG_RTE_LIBRTE_ENIC_PMD) += enic
DIRS-$(CONFIG_RTE_LIBRTE_PMD_FAILSAFE) += failsafe
DIRS-$(CONFIG_RTE_LIBRTE_FM10K_PMD) += fm10k
DIRS-$(CONFIG_RTE_LIBRTE_I40E_PMD) += i40e
DIRS-$(CONFIG_RTE_LIBRTE_IXGBE_PMD) += ixgbe
DIRS-$(CONFIG_RTE_LIBRTE_LIO_PMD) += liquidio
DIRS-$(CONFIG_RTE_LIBRTE_MLX4_PMD) += mlx4
DIRS-$(CONFIG_RTE_LIBRTE_MLX5_PMD) += mlx5
DIRS-$(CONFIG_RTE_LIBRTE_MRVL_PMD) += mrvl
DIRS-$(CONFIG_RTE_LIBRTE_NFP_PMD) += nfp
DIRS-$(CONFIG_RTE_LIBRTE_BNXT_PMD) += bnxt
DIRS-$(CONFIG_RTE_LIBRTE_PMD_NULL) += null
DIRS-$(CONFIG_RTE_LIBRTE_OCTEONTX_PMD) += octeontx
DIRS-$(CONFIG_RTE_LIBRTE_PMD_PCAP) += pcap
DIRS-$(CONFIG_RTE_LIBRTE_PPFE_PMD) += ppfe
DIRS-$(CONFIG_RTE_LIBRTE_QEDE_PMD) += qede
DIRS-$(CONFIG_RTE_LIBRTE_PMD_RING) += ring
DIRS-$(CONFIG_RTE_LIBRTE_SFC_EFX_PMD) += sfc
DIRS-$(CONFIG_RTE_LIBRTE_PMD_SZEDATA2) += szedata2
DIRS-$(CONFIG_RTE_LIBRTE_PMD_TAP) += tap
DIRS-$(CONFIG_RTE_LIBRTE_THUNDERX_NICVF_PMD) += thunderx
DIRS-$(CONFIG_RTE_LIBRTE_VIRTIO_PMD) += virtio
DIRS-$(CONFIG_RTE_LIBRTE_VMXNET3_PMD) += vmxnet3

ifeq ($(CONFIG_RTE_LIBRTE_KNI),y)
DIRS-$(CONFIG_RTE_LIBRTE_PMD_KNI) += kni
endif

ifeq ($(CONFIG_RTE_LIBRTE_SCHED),y)
DIRS-$(CONFIG_RTE_LIBRTE_PMD_SOFTNIC) += softnic
endif # $(CONFIG_RTE_LIBRTE_SCHED)

ifeq ($(CONFIG_RTE_LIBRTE_VHOST),y)
DIRS-$(CONFIG_RTE_LIBRTE_PMD_VHOST) += vhost
endif # $(CONFIG_RTE_LIBRTE_VHOST)

ifeq ($(CONFIG_RTE_LIBRTE_MRVL_PMD),y)
ifeq ($(CONFIG_RTE_LIBRTE_CFGFILE),n)
$(error "RTE_LIBRTE_CFGFILE must be enabled in configuration!")
endif
endif

include $(RTE_SDK)/mk/rte.subdir.mk
