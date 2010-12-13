# see http://wiki.lyx.org/Layouts/CreatingLayouts for info on how to
# create things for this

cmake_minimum_required(VERSION 2.8)
#project(lyx-support NONE)

find_file(INSTALL_LYX_DIR
	NAMES
	.lyx
	lyx
	PATHS
	"$ENV{HOME}"
	"$ENV{UserProfile}")
find_file(INSTALL_TEX_DIR
	NAMES
	.texmf
	texmf
	PATHS
	"$ENV{HOME}"
	"$ENV{UserProfile}")

#set(INSTALL_LYX_DIR "$ENV{HOME}/.lyx")

if(NOT INSTALL_LYX_DIR)
	message(FATAL_ERROR "Must have a LyX user directory specified!")
endif()

if(NOT INSTALL_TEX_DIR)
	message(FATAL_ERROR "Must have a TeX user directory specified!")
endif()

set(LYX_TEMPLATES_DIR "${INSTALL_LYX_DIR}/templates")
set(LYX_LAYOUTS_DIR "${INSTALL_LYX_DIR}/layouts")
set(BIBTEX_BST_DIR "${INSTALL_TEX_DIR}/bibtex/bst")
set(LATEX_CLS_DIR "${INSTALL_TEX_DIR}/tex/latex")

add_subdirectory(asme)
add_subdirectory(ieee-vgtc-conferences)
