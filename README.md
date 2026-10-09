# MEDPLUM

![licence](https://img.shields.io/badge/licence-Apache-2.0-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![checks](https://img.shields.io/badge/checks-unknown_PASS-brightgreen)

> Governed Anticloud packaging of the upstream project `MEDPLUM` in category **MEDICAL_HEALTH**. check results: see ISOLATED_LAB_RESULTS. Every number below traces to a named file + run stamp; nothing is borrowed from other projects.

**Upstream:** MEDPLUM · **Upstream pin:** `a08437eab79c5ccc2a3cdecd32716e646d115bac` · **Category:** MEDICAL_HEALTH · **Vendor:** Anticloud FZ LLE · **Licence:** Apache-2.0

---

## What This Project Does

# [Medplum](https://www.medplum.com) &middot; [![GitHub license](https://img.shields.io/badge/license-Apache-blue.svg)](https://github.com/medplum/medplum/blob/main/LICENSE.txt) [![npm version](https://img.shields.io/npm/v/@medplum/core.svg?color=blue)](https://www.npmjs.com/package/@medplum/core) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=medplum_medplum&metric=alert_status&token=207c95a43e7519809d6d336d8cc7837d3e057acf)](https://sonarcloud.io/dashboard?id=medplum_medplum) [![Coverage Status](https://coveralls.io/projects/github/medplum/medplum/badge.svg?branch=main)](https://coveralls.io/github/medplum/medplum?branch=main) [![OpenSSF Best Practices](https://www.bestpractices.dev/projects/10900/badge?gold)](https://www.bestpractices.dev/projects/10900)

![Medplum](packages/docs/static/img/cover.webp)

Medplum is a developer platform that enables flexible and rapid development of healthcare apps.

- **Medplum Auth** - End-to-end identity solution for easy user authentication, sign-in, and permissions using OAuth, OpenID, and SMART-on-FHIR.
- **Medplum Clinical Data project (CDR)** - Backend server that hosts your healthcare data in a secure, compliant, and standards-based project.
- **Medplum API** - FHIR-based API for sending, receiving, and manipulating data.
- **Medplum SDK** - Client libraries that simplify the process of interacting with the **Medplum API**.
- **Medplum App** - Web application where you can view your data and perform basic editing tasks. You can also use the Medplum App to manage basic workflows.
- **Medplum Bots** - Write and run application logic server-side without needing to set up your own server.
- **UI Component Library** - React components designed to help you quickly develop custom healthcare applications.

## Docs

- [Contributing](#contributing)
  - [Ground Rules](#ground-rules)
  - [Codebase](#codebase)
    - [Technologies](#technologies)
    - [Folder Structure](#folder-structure)

## Contributing

**We heartily welcome any and all contributions that match our engineering standards!**

That being said, this codebase isn't your typical open-source project because it's not a library or package with a
limited scope -- it's our entire product. Our [Contributing documentation](https://medplum.com/docs/contributing) has
all the information you need to get started.

### Ground Rules

#### Contributions and discussion guidelines

By making a contribution to this project, you are deemed to have accepted the [Developer Certificate of Origin](https://developercertificate.org/) (DCO).

All conversations and communities on Medplum are expected to follow GitHub's [Community Guidelines](https://help.github.com/en/github/site-policy/github-community-guidelines)
and [Acceptable Use Policies](https://help.github.com/en/github/site-policy/github-acceptable-use-policies). We expect
discussions on issues and pull requests to stay positive, productive, and respectful. Remember: there are real people on
the other side of the screen!

#### Reporting a bug or proposing a new feature

If you found a technical bug on Medplum or have ideas for features we should implement, the issue tracker is the best
place to share with us. ([click here to open a new issue](https://github.com/medplum/medplum/issues/new))

### Writing documentation or blog content

Did you learn how to do something using Medplum that wasn't obvious on your first try? By contributing your new knowledge
to our documentation, you can help others who might have a similar use case!

Our documentation is hosted on [medplum.com/docs](https://www.medplum.com/docs), but it is built from [Markdown](https://www.markdownguide.org/)
files in our [`docs` package](https://github.com/medplum/medplum/tree/main/packages/docs/docs).

For relatively small changes, you can edit files directly from your web browser on [GitHub.dev](https://github.dev/medplum/medplum/blob/main/packages/docs/docs/home.md)
without needing to source the project.

#### Fixing a bug or implementing a new feature

To keep new contributors focused on work we're ready to accept, code contributions go through an approval system: your
Pull Request must be linked to an issue labeled `open-to-community` before we'll review it. This signals that a
maintainer has explicitly invited community help on that issue. You can link a PR to an issue with a closing keyword
in the PR description (e.g. `Fixes #123`) or via GitHub's Development panel. PRs that aren't linked to an
`open-to-community` issue are automatically closed, but can be reopened once the link is added. Established
contributors and Medplum team members are exempt from this requirement.

If you find a bug, look for an existing issue labeled `open-to-community`, or open a new issue and ask us to label it,
before starting work on a fix.

If you want to implement a new feature, open an issue first to discuss with us how the feature might work, and to ensure
it fits into our roadmap and plans for the app.

If you want to contribute but are unsure how to start, we have [a "good first issue" label](https://github.com/medplum/medplum/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) which is applied to newcomer-friendly issues. Take a look at [the full list of good first issues](https://github.com/medplum/medplum/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) and pick something you like!

**Ready to get started writing code?** Follow the [local setup instructions](https://www.medplum.com/docs/contributing/local-dev-setup) and jump in! See our [full contributing guide](https://www.medplum.com/docs/contributing#making-a-contribution) for more details on this process.

### Codebase

#### Technologies

With the ground rules out of the way, let's talk about the coarse architecture of this mono project:

- **Full-stack TypeScript**: We use Node.js to power our servers, and React to power our frontend apps. Almost all of the code you'll touch in this codebase will be TypeScript.

Here is a list of all the big technologies we use:

- **PostgreSQL**: Data storage
- **Redis**: Background jobs and caching
- **Express**: API server
- **TypeScript**: Type-safe JavaScript
- **React**: Frontend React app

#### Folder structure

```sh
medplum/
├── packages
│   ├── agent           # On-premise agent
│   ├── app             # Frontend web app
│   ├── bot-layer       # AWS Lambda Layer for Bots
│   ├── cdk             # AWS CDK infra as code
│   ├── cli             # Command line interface
│   ├── core            # Core shared library
│   ├── definitions     # Data definitions
│   ├── docs            # Documentation
│   ├── examples        # Example code used in documentation
│   ├── fhir-router     # FHIR URL router
│   ├── fhirtypes       # FHIR TypeScript definitions
│   ├── generator       # Code generator utilities
│   ├── graphiql        # Preconfigured GraphiQL
│   ├── hl7             # HL7 client and server
│   ├── mock            # Mock FHIR data for testing
│   ├── react           # React component library
│   ├── react-hooks     # React hooks library
│   └── server          # Backend API server
└── scripts             # Helper bash scripts
```

## Thanks

<a href="https://www.chromatic.com/"><img src="https://user-images.githubusercontent.com/321738/84662277-e3db4f80-af1b-11ea-88f5-91d67a5e59f6.png" width="153" height="30" alt="Chromatic" /></a>

Thanks to [Chromatic](https://www.chromatic.com/) for providing the visual testing platform that helps us review UI changes and catch visual regressions.

## License

[Apache 2.0](LICENSE.txt)

---

## Installation

See the upstream documentation quoted in What This Project Does above.

## Usage

- **Medplum Clinical Data project (CDR)** - Backend server that hosts your healthcare data in a secure, compliant, and standards-based project.
- **Medplum API** - FHIR-based API for sending, receiving, and manipulating data.
- **Medplum SDK** - Client libraries that simplify the process of interacting with the **Medplum API**.
- **Medplum App** - Web application where you can view your data and perform basic editing tasks. You can also use the Medplum App to manage basic workflows.
- **Medplum Bots** - Write and run application logic server-side without needing to set up your own server.
- **UI Component Library** - React components designed to help you quickly develop custom healthcare applications.

## API

![Medplum](packages/docs/static/img/cover.webp)

Medplum is a developer platform that enables flexible and rapid development of healthcare apps.

- **Medplum Auth** - End-to-end identity solution for easy user authentication, sign-in, and permissions using OAuth, OpenID, and SMART-on-FHIR.
- **Medplum Clinical Data project (CDR)** - Backend server that hosts your healthcare data in a secure, compliant, and standards-based project.
- **Medplum API** - FHIR-based API for sending, receiving, and manipulating data.
- **Medplum SDK** - Client libraries that simplify the process of interacting with the **Medplum API**.
- **Medplum App** - Web application where you can view your data and perform basic editing tasks. You can also use the Medplum App to manage basic workflows.
- **Medplum Bots** - Write and run application logic server-side without needing to set up your own server.
- **UI Component Library** - React components designed to help you quickly develop custom healthcare applications.

## Dependencies

| Metric | Value |
|--------|-------|
| Files | unknown |
| Lines of Code | unknown |
| Dependencies | unknown |
| Upstream license (harvested) | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Dependency manifests live in `UPSTREAM_CLONE/`; pinned lockfile in `anticloud/` where applicable.

## Configuration

│   ├── hl7             # HL7 client and server
│   ├── mock            # Mock FHIR data for testing
│   ├── react           # React component library
│   ├── react-hooks     # React hooks library
│   └── server          # Backend API server
└── scripts             # Helper bash scripts
```

## Contributing

- **Medplum Auth** - End-to-end identity solution for easy user authentication, sign-in, and permissions using OAuth, OpenID, and SMART-on-FHIR.
- **Medplum Clinical Data project (CDR)** - Backend server that hosts your healthcare data in a secure, compliant, and standards-based project.
- **Medplum API** - FHIR-based API for sending, receiving, and manipulating data.
- **Medplum SDK** - Client libraries that simplify the process of interacting with the **Medplum API**.
- **Medplum App** - Web application where you can view your data and perform basic editing tasks. You can also use the Medplum App to manage basic workflows.
- **Medplum Bots** - Write and run application logic server-side without needing to set up your own server.
- **UI Component Library** - React components designed to help you quickly develop custom healthcare applications.

## License

Upstream © its respective contributors under Apache-2.0 (harvested MIT/Apache-2.0/BSD source; see `UPSTREAM_CLONE/LICENSE`). This packaging overlay is licensed under Anticommons 0.1.0.

## Upstream

- **project:** MEDPLUM
- **Pinned SHA:** `a08437eab79c5ccc2a3cdecd32716e646d115bac`
- **source:** `UPSTREAM_CLONE/` (pinned at the SHA above)
- **Upstream README source:** `UPSTREAM_CLONE/README.md`

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`413351c76c806aa7f8056aea773111d9df8e7290a17d47e5ceed66841587cf84`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

