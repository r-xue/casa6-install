# Makefile for building Sphinx documentations

# You can set these variables from the command line.
SPHINXOPTS    = -v -j auto
SPHINXBUILD   = python -msphinx
SPHINXPROJ    = casa6_install
SOURCEDIR     = source
BUILDDIR      = _build

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

github:
	@rm -rf _build/html
	@make html
	@rm -rf html
	@mkdir html
	@cp -a _build/html/* html/
