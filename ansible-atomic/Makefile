vault_file = .vault_pass_2000
config_files = hosts.yml $(vault_file)

init : $(config_files)

hosts.yml : hosts.yml.sample
	cp $< $@

$(vault_file) :
	@if [ ! -f $(vault_file) ]; then \
		echo "Password is missing in $(vault_file) file!"; \
		echo "PLACE PASSWORD HERE" > $(vault_file); \
		chmod g-rwx,o-rwx $(vault_file); \
	fi
