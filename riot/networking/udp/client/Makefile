APPLICATION = posix_client

BOARD ?= native

RIOTBASE ?= $(CURDIR)/../../../RIOT

SERVER_PORT ?= 8888
SERVER_ADDR ?= fe80::1

# Import radio driver module
USEMODULE += gnrc_netdev_default
USEMODULE += auto_init_gnrc_netif

# Import network modules
USEMODULE += gnrc_ipv6_default
USEMODULE += gnrc_sock_udp

# Import posix sockets


DEVELHELP ?= 1

CFLAGS += -DSERVER_PORT=$(SERVER_PORT)
CFLAGS += -DSERVER_ADDR=\"$(SERVER_ADDR)\"

include $(RIOTBASE)/Makefile.include

# Set a custom channel if needed
include $(RIOTMAKE)/default-radio-settings.inc.mk
