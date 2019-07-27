project('fake-program', 'c',  version : '0.0.1', license : 'MIT')
executable('fake-program', 'main.c', install : true)

conf_data = configuration_data()
conf_data.set('version', meson.project_version())

configure_file(
    input : 'fake-program.1.in',
    output : 'fake-program.1',
    configuration : conf_data
)
install_man(fake-program.1)
