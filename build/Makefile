#####################################################################################
#   _____ _           _   _                    _   _____            _               #
#  / ____| |         | | | |                  | | |  __ \          | |              #
# | (___ | |__   __ _| |_| |_ ___ _ __ ___  __| | | |__) |___  __ _| |_ __ ___  ___ #
#  \___ \| '_ \ / _` | __| __/ _ \ '__/ _ \/ _` | |  _  // _ \/ _` | | '_ ` _ \/ __|#
#  ____) | | | | (_| | |_| ||  __/ | |  __/ (_| | | | \ \  __/ (_| | | | | | | \__ \#
# |_____/|_| |_|\__,_|\__|\__\___|_|  \___|\__,_| |_|  \_\___|\__,_|_|_| |_| |_|___/#
#          _____                        ____             _                  _       #
#         / ____|                      |  _ \           | |                | |      #
#        | |  __  __ _ _ __ ___   ___  | |_) | __ _  ___| | _____ _ __   __| |      #
#        | | |_ |/ _` | '_ ` _ \ / _ \ |  _ < / _` |/ __| |/ / _ \ '_ \ / _` |      #
#        | |__| | (_| | | | | | |  __/ | |_) | (_| | (__|   <  __/ | | | (_| |      #
#         \_____|\__,_|_| |_| |_|\___| |____/ \__,_|\___|_|\_\___|_| |_|\__,_|      #
#####################################################################################
#
# Makefile for building, running, and testing
#

# Application versions
BASE_VERSION = 0.0.1

# Gets the directory containing the Makefile
BUILD_DIR = $(shell dirname $(realpath $(firstword $(MAKEFILE_LIST))))

# Root code directory
ROOT_DIR = $(realpath $(BUILD_DIR)/..)

# Directory containing applications
BASE_APP_DIR = $(realpath $(ROOT_DIR)/cmd)

# Binary output directory
BIN_DIR = $(realpath $(ROOT_DIR)/bin)

# Entrypoint for applications
APP_MAIN = $(BASE_APP_DIR)/game-backend/main.go

#   _____                    _
#  |_   _|                  | |
#    | | __ _ _ __ __ _  ___| |_ ___
#    | |/ _` | '__/ _` |/ _ \ __/ __|
#    | | (_| | | | (_| |  __/ |_\__ \
#    \_/\__,_|_|  \__, |\___|\__|___/
#                  __/ |
#                 |___/

build:
	go build -o $(BIN_DIR)/game-backend $(APP_MAIN)

test:
	ginkgo $(ROOT_DIR)/... -covermode atomic --randomize-all