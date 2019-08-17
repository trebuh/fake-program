project('fake-program', 'c',  version : '0.0.1', license : 'MIT')
executable('fake-program', 'main.c', install : true)

conf_data = configuration_data()
conf_data.set('version', meson.project_version())
conf_data.set('name', meson.project_name())

man_page = configure_file(
    input : 'fake-program.1.in',
    output : 'fake-program.1',
    configuration : conf_data
)

install_man(man_page)

configure_file(
    input : 'fake-program.service.in',
    output : 'fake-program.service',
    configuration : conf_data,
    install_dir : '/etc/systemd/system/'
    install_mode: ['rw-r--r--', 'root', 'root']
)
