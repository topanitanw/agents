SHELL := /bin/bash

PI_GLOBAL_DIR_PATH=~/.pi/agent
PI_THEME_DIR_PATH=$(PI_GLOBAL_DIR_PATH)/themes

.PHONY: install
install:
	mkdir -p $(PI_THEME_DIR_PATH)
	ln -sf `realpath settings.json` $(PI_GLOBAL_DIR_PATH)/.
	ln -sf `realpath zenburn.json` $(PI_THEME_DIR_PATH)/.
	@$(MAKE) test

.PHONY: test
test:
	find $(PI_GLOBAL_DIR_PATH) -type l -iname "*.json" -exec ls -alh {} \;
