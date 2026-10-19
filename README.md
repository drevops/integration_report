<div align="center">
  <a href="" rel="noopener">
  <img width=200px height=200px src="logo.png" alt="Integration Report Drupal module"></a>
</div>

<h1 align="center">Integration Report Drupal module</h1>

<div align="center">

[![GitHub Issues](https://img.shields.io/github/issues/drevops/integration_report.svg)](https://github.com/drevops/integration_report/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/drevops/integration_report.svg)](https://github.com/drevops/integration_report/pulls)
[![Test](https://github.com/drevops/integration_report/actions/workflows/test.yml/badge.svg)](https://github.com/drevops/integration_report/actions/workflows/test.yml)
[![codecov](https://codecov.io/gh/drevops/integration_report/graph/badge.svg)](https://codecov.io/gh/drevops/integration_report)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/drevops/integration_report)
![License: GPL-2.0-or-later](https://img.shields.io/badge/license-GPL--2.0--or--later-orange.svg)
![Renovate](https://img.shields.io/badge/renovate-enabled-green?logo=renovatebot)

![PHP 8.3](https://img.shields.io/badge/PHP-8.3-777BB4.svg)
![PHP 8.4](https://img.shields.io/badge/PHP-8.4-777BB4.svg)
![PHP 8.5](https://img.shields.io/badge/PHP-8.5-777BB4.svg)
![Drupal 10](https://img.shields.io/badge/Drupal-10-009CDE.svg)
![Drupal 11](https://img.shields.io/badge/Drupal-11-006AA9.svg)
![Drupal 12](https://img.shields.io/badge/Drupal-12-004B7A.svg)

</div>

---

![screenshot](https://user-images.githubusercontent.com/378794/39668688-daf598bc-5117-11e8-9d15-5459278d164e.png)

## Why?

If your website has 3rd-party integration with one or multiple 3rd-party
services via API endpoints, this module allows to call the endpoints and
see all the response information within a single page.

You may also implement status check on behalf of any other Drupal module that
does not have such information page.

## Features

- Single page for all status checks.
- `<iframe>`-based status checks (useful for SSO with redirects).

## Getting started

1. Extend `IntegrationReport` class with your 3rd-party endpoint request
   methods.
2. Register this class as a service in your custom module and tag it:

        services:
          example_integration_report:
            class: Drupal\example\ExampleIntegrationReport
            tags:
              - { name: integration_report }

3. Go to `/admin/reports/integrations` to check the status.

Refer to [integration_report.api.php](integration_report.api.php) and
`modules/integration_report_example` for an implementation example.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for local development, building the site, checking coding standards, and running the tests.

---
_This repository was created using the [Eddy](https://github.com/drevops/eddy) project template_
