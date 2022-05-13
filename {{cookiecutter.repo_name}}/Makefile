FIRST_COMMIT := $(shell git log >/dev/null 2>&1; echo $$?)

init:
	@terraform init -upgrade

plan:
	@terraform plan

apply:
	@terraform apply

docs:
	@terraform-docs .

setup: docs
ifneq ($(FIRST_COMMIT), 0)
	@git init
	@pre-commit install
	@git add .
	@git commit -m "first commit"
	@git branch -M main
	@git remote add origin git@github.com:ponceps/{{cookiecutter.repo_name}}.git
	@git push -u origin main
else
	$(error Setup already done)
endif
