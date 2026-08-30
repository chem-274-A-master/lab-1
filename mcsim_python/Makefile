
.PHONY: environment remove-env install uninstall test # .PHONY marks targets that run commands rather than represent files.

MODULE=mcsim
ENVIRONMENT=chem274A_lab1

environment:
	conda create -n $(ENVIRONMENT) "python=3.14" --yes
	conda install -c conda-forge jupyterlab numpy matplotlib pandas --name $(ENVIRONMENT) --yes

remove-env:
	conda remove --name $(ENVIRONMENT) --all --yes

install: ## install the package to the active Python's site-packages
	pip install .

dev-install:
	pip install -e .

uninstall: ## uninstall the package
	pip uninstall --yes $(MODULE)

test: 
	pytest -v
