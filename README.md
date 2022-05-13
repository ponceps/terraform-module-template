# terraform-module-template

[Cookiecutter](https://github.com/cookiecutter/cookiecutter) template for a Terraform module.

## Usage

### Setup
Install the latest Cookiecutter if you haven't installed it yet:

```bash
pip install -U cookiecutter
```

Or, if you are using Mac OS:

```bash
brew install cookiecutter
```

For alternate installations, see [cookiecutter installation](https://cookiecutter.readthedocs.io/en/latest/installation.html).


Generate a Terraform module:

```bash
cookiecutter git@github.com:ponceps/terraform-module-template
```

### Pushing to Github

[Create a new repository on Github](https://help.github.com/articles/creating-a-new-repository/) and at the module directory:

```bash
make setup
```

## Module Conventions
- **GitHub**: the module must be on GitHub and must be a private repo.
- **Named terraform-&lt;PROVIDER&gt;-&lt;NAME&gt;**: module repositories must use this three-part name format, where <NAME> reflects the type of infrastructure the module manages and <PROVIDER> is the main provider where it creates that infrastructure. The <NAME> segment can contain additional hyphens. Examples: terraform-google-vault or terraform-aws-ec2-instance.
- **x.y.z tags for releases**: release tag names must be a semantic version prefixed with a v. For example, v1.0.4.
