program_name = 'jack-connection-manager'

if get_option('node').startswith(playername)
    install_subdir('player', strip_directory : true, install_dir : get_option('sysconfdir') / program_name + install_postfix)
elif get_option('node').startswith(renderername + '01')
    install_subdir('renderer-ambi', strip_directory : true, install_dir : get_option('sysconfdir') / program_name + install_postfix)
elif get_option('node').startswith(renderername)
    install_subdir('renderer-wfs', strip_directory : true, install_dir : get_option('sysconfdir') / program_name + install_postfix)
endif

if get_option('versioned_install')
meson.add_install_script(
	'sh', '-c',
	'ln -s -f -n @0@ @1@'.format(
        get_option('prefix') / get_option('sysconfdir') / program_name + install_postfix + '/',
        get_option('prefix') / get_option('sysconfdir') / program_name)
)
endif