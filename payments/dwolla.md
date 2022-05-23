# Dwolla

## `.env`

Requirements:

* All repositories _must_ include a `.env` file in the root of the `main` branch. This file should include all of the items:

```
key
Secret

```

* You can obtain a Dwolla Sandbox API Key and Secret by signing up for a free [Dwolla Sandbox Account](https://accounts-sandbox.dwolla.com/login)

## `.gitignore`

Requirements:

* All repositories _must_ include a `.gitignore` file in the root of the `main` branch. This file should include all of the items:

```
.env

```

Rationale:

* Your .env file will contain sensitive information like your Dwolla key and secret, which should never be shared.

Exceptions:

* None

## Test Environment

Requirments:

* When working in Dwolla's test environment, students should only use fake data, this includes customer names. Below you will find a link of how to format this data:

[Creating a Customer](https://developers.dwolla.com/guides/receive-money/create-a-customer#step-1a-create-the-customer)

[Adding a bank funding source](https://developers.dwolla.com/guides/send-money/add-funding-source#step-2a-adding-a-bank-to-the-receive-only-user): Routing numbers must be 9 digits long, account numbers must be 4 - 17 digits long.

Rationale:

* Using real data in Dwolla's API while in the testing environment is highly discouraged. The functionality to delete certain data isn’t supported as per the data retention guidelines that Dwolla is subject to within the United States. It is important to not use sensitive information while testing in the Sandbox.

Exceptions:

* None

## Support

Requirments:

Below is a list of resources available for support in projects using the Dwolla API:

- [Sandbox](https://accounts-sandbox.dwolla.com/login): Email _must_ be the student's `lambdastudents.com` email address in lowercase

- [Postman Collection](https://app.getpostman.com/run-collection/e946a89ed19313cce582)

- [Dev Portal](https://developers.dwolla.com/?utm_source=prod&utm_medium=launchpad&utm_campaign=dwolla-overview)

- [Dev Docs](https://docs.dwolla.com/)

- [Support Forum](https://discuss.dwolla.com/)

- [Dwolla Dev YouTube](https://www.youtube.com/channel/UCPuFDQV7b_CeHPY1nbIbrWA)

- Developer Advocate: Kelly Moreira, kmoreira@dwolla.com


Rationale:

* These are resources Dwolla client developers utilize to integrate Dwolla into their product. Lambda School students will become familiar with the common behavorial patterns of a payments intgration following these resources. 

* Dwolla clients also have an assigned Developer Advocate during their integration process. Kelly has been assigned as the Developer Advocate for any Lambda Labs project that wishes to incorporate Dwolla.

* Student emails _must_ be the student's `lambdastudents.com` email in order to prevent production marketing to students

Exceptions:

* Other open sourced resources available online