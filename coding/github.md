# Github

## (GH-100) One GitHub Organization

Code for all student GitHub projects must be stored in the [BloomTech Labs GitHub organization](https://github.com/bloomtech-labs)

Rationale:

* Centralizing code into a single organization allows for easier management.

## (GH-101) Organization Roles

BloomTech staff will have the `Owner` role. All other organization members will have the `Member` role.

Rationale:

* Least privilege

Exceptions:

* None

## (GH-102) GitHub Cohort Admin Teams

Each Labs cohort must have a corresponding GitHub Cohort Admin team named as follows:

* `<Cohort> - Admins` (Example: `Labs 20 - Admins`)

Team structure:

* All TPLs
* All repositories related to the cohort

Rationale:

* TPLs need administrative access to _all_ of the repositories related to a specific cohort. This allows TPLs to cover for each other and handle administrative tasks on the repos when another is not available.

Exceptions:

* None

## (GH-200) Dedicated GitHub Teams

Each project team will have its own dedicated GitHub team within the BloomTech Labs organization. Each team should be named as follows:

`<Cohort> - <Product> - <Team Letter>` (Example: `Labs 20 - Brew Plans - C`)

## Team structure

| Member  | Role       |
| ------- | ---------- |
| APL     | Maintainer |
| TPL     | Admin      |
| Student | Member     |

* Repositories: All repositories related to the cohort

Rationale:

* Project-specific teams allow for easier application of precise (least privilege) permissions as well as easier provisioning and de-provisioning as cohorts begin and end.

Exceptions:

* None

## (GH-300) GitHub Repo Naming

GitHub repos shall be named in all lowercase using the following convention:

* Repo names must be all lowercase, using only alphanumeric characters and hyphens
* Format: `<product>-<team letter>-<purpose>-<postfix>`
  * The `Product` name should be stripped of special characters, shortened or otherwise made to be more readable and it must remain consistent across repositories.
  * The `Purpose` must be one of the following
    * `fe` for a front-end repository
    * `be` for a back-end repository
    * `ds` for a data science repository
    * `mobile` for a cross-platform mobile repository
    * `ios` for an iOS specific mobile repository
    * `android` for an Android specific mobile repository
    * `site` for a static website associated with the product
  * The `Postfix` is an arbitrary string that can be appended when multiple repositories with the same purpose are required for a particular product.

### Examples

| Product    | Team Letter | Purpose          | Postfix | Repo Name             |
| ---------- | ----------- | ---------------- | ------- | --------------------- |
| EcoSoap    | A           | Front-end SPA    |         | ecosoap-a-fe          |
| Brew Plans | B           | iOS App          |         | brew-plans-b-ios      |
| Megamind   | D           | DS API           |         | megamind-d-ds         |
| Megamind   | D           | Jupyter Notebook | Jupyter | megamind-d-ds-jupyter |

Rationale:

*   GitHub repositories have no mechanism for storing metadata, so the product

    name and purpose must be encoded in the repo name.

Exceptions:

* None

## (GH-310) GitHub Templates

All new GitHub repositories must be created using the appropriate Labs Scaffolding:

* [React SPA](https://docs.labs.lambdaschool.com/labs-spa-starter/)
* [Node.js API](https://docs.labs.lambdaschool.com/api/)
* [DS API](https://docs.labs.lambdaschool.com/data-science/)

Rationale:

* Consistency is critical for managing a highly complex organization at scale. Starting from the same basic template helps to maintain this consistency.

Exceptions:

* None

## (GH-311) Require GitHub Branch Protection setup for the `main` branch

All GitHub repositories must be setup with [branch protection](https://help.github.com/en/github/administering-a-repository/about-protected-branches) enabled for the `main` branch as follows:

* Required approving reviews: 2 (or more)
* Require status checks to be passing before merging (enabled)
  * Require branches to be up to date before merging (enabled)
* Include administrators (enabled)

Rationale:

* The `main` branch is a direct reflection of the code that is deployed to the production environment. As such, it is crucial that all code headed to the `main` branch be carefully reviewed and tested before a merge.

Exceptions:

* None

## (GH-320) GitHub Repo Licensing

The README in the root of each GitHub repository must advertise that the code is maintained under the MIT license.

* There must be a file named LICENSE in the root of the directory using the MIT license format as described here: [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)
  * Use the year the project was created for the year
  * Use 'BloomTech' as the copyright holder

Rationale:

* Code written during Labs projects must be maintained as open-source so that it can be reference by hiring managers considering BloomTech students as candidates.
* The MIT license is very permissive and provides opportunities for student developed code to be reused and expanded by the open-source community.

Exceptions:

* None

## (GH-400) GitHub Branch Cleanup

Once a branch has been merged into `main` it should be immediately deleted to keep your repository clean and manageable.

* The "Automatically delete head branches" option must be enabled fo all repos: [https://docs.github.com/en/free-pro-team@latest/github/administering-a-repository/managing-the-automatic-deletion-of-branches](https://github.com/Lambda-School-Labs/gitbook-standards/tree/bca2e4ce4272774d67dd726463388e137a06f202/coding/instructions/README.md)

Rationale:

* Once a branch has been merged to `main` the change is complete. Any additional changes should be made on a new branch. Too many branches can lead to confusion and merge conflicts.

Exceptions:

* None
