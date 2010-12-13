install(FILES asme2e.cls
	DESTINATION "${LATEX_CLS_DIR}/asme2e/")

install(FILES asme_journals/asme_journals.bst
	DESTINATION "${BIBTEX_BST_DIR}/asme_journals/")

install(FILES asmems4/asmems4.bst
	DESTINATION "${BIBTEX_BST_DIR}/asmems4/")

install(FILES asme2e.layout
	DESTINATION "${LYX_LAYOUTS_DIR}")
	
install(FILES "ASME Paper Template.lyx"
	DESTINATION "${LYX_TEMPLATES_DIR}")
