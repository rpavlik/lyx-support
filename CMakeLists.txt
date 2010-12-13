# see http://wiki.lyx.org/Layouts/CreatingLayouts for info on how to
# create things for this

cmake_minimum_required(VERSION 2.8)
#project(lyx-support NONE)

set(INSTALL_LYX_DIR "$ENV{HOME}/.lyx")
set(INSTALL_TEX_DIR "$ENV{HOME}/texmf")

set(LYX_TEMPLATES_DIR "${INSTALL_LYX_DIR}/templates")
set(LYX_LAYOUTS_DIR "${INSTALL_LYX_DIR}/layouts")
set(BIBTEX_BST_DIR "${INSTALL_TEX_DIR}/bibtex/bst")
set(LATEX_CLS_DIR "${INSTALL_TEX_DIR}/tex/latex")

add_subdirectory(asme)
add_subdirectory(ieee-vgtc-conferences)
