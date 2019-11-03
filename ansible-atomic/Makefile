config_files = hosts.yml .vault_pass

init : $(config_files)

hosts.yml : hosts.yml.sample
	cp $< $@

.vault_pass :
	@if [ ! -f .vault_pass ]; then \
		echo "Password is missing in .vault_pass file!"; \
		echo "PLACE PASSWORD HERE" > .vault_pass; \
		chmod g-rwx,o-rwx .vault_pass; \
	fi
