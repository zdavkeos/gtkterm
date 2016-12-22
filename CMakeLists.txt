cmake_minimum_required(VERSION 3.4)

project(GtkTerm C)

set(VERSION 0.99.x)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK3 REQUIRED gtk+-3.0)
pkg_check_modules(VTE REQUIRED vte-2.91)

include_directories(
  ${GTK3_INCLUDE_DIRS}
  ${VTE_INCLUDE_DIRS})

link_directories(
  ${GTK3_LIBRARY_DIRS}
  ${VTE_LIBRARY_DIRS})

add_definitions(
  -DVERSION="${VERSION}"
  -DPACKAGE="gtkterm"
  -DLOCALEDIR="po"
  ${GTK3_CFLAGS_OTHER}
  ${VTE_CFLAGS_OTHER})

set(gtkterm_SOURCES
  src/i18n.c
  src/widgets.c
  src/cmdline.c
  src/parsecfg.c
  src/term_config.c
  src/macros.c
  src/fichier.c
  src/buffer.c
  src/serie.c
  src/gtkterm.c
  src/logging.c)

add_executable(gtkterm ${gtkterm_SOURCES})

target_link_libraries(gtkterm
  ${GTK3_LIBRARIES}
  ${VTE_LIBRARIES})
