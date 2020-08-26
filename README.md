# Home

This document describes the engineering standards that teams working in Lambda X must comply with. Adherence to these standards is critical to the continued success of the Lambda X organization, as they allow us to more effectively manage the scores of teams working across hundreds of products.

### Topics

This guide is divided into separate topics. A topic corresponds to a specific area of concern in software engineering. For example, [Programming Languages](coding/programming-languages.md) is a topic.

### Standards

The standards in this guide do not cover all choices in technology. Many are purposely omitted as they are not considered impactful to the quality of the overall program.

However, this guide is exclusive, in that, if a technology choice is _not_ mentioned as part of a topic, you can assume the use of that technology is prohibited. When in doubt, please open an issue or submit a PR to start a discussion.

### Contributing

These standards will morph over time as we adapt to the ever-changing technology landscape. In addition, the stardards will embrace a subset of all of the available technologies, so that teams have options when making technical decisions. In order to ensure that these documents are inclusive of the needs of all Labs groups, each new standard or change to an existing standard will be ratified by approval from 3 Labs Tech Leads.

These standards will morph over time as we adapt to the ever-changing technology landscape. Also, the standards will embrace a subset of all of the available technologies, so that teams have options when making technical decisions. To ensure that these documents are inclusive of the needs of all Lab groups, each new standard or change to an existing standard will be ratified by approval from 3 Labs Tech Leads.

See [Writing Standards](writing-standards.md) for more details on the format for standards.

#### Setup your local enviornment

All steps below are based on the use of [pipenv](https://pipenv.kennethreitz.org/en/latest/)

* on mac: `> brew install pipenv`

  The GitHub actions still require a `requirements.txt` file so if you add anything to the `Pipfile` you will also need to add it to the `requirements.txt` file.

1. Install all dependencies and set up a python virtual env
   * `> pipenv install --dev`
2. Start a pipenv shell
   * `> pipenv shell`
3. Run the mkdocs server to build and view you local changes
   * `> mkdocs serve`
   * Now open browser to `http://localhost:8000`
4. Install markdown linter
   * `> npm install -g markdownlint-cli`
5. Run the markdown linter before commiting
   * `> markdownlint -c .markdownlint.json .`

     !!! Warning Please be aware that the `mkdocs serve` command serves the files directly from the `docs` folder and does not build the `site` folder as does the `mkdocs build` command. This means that relative paths may cause a warning.

