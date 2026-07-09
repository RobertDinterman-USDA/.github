# Rural Development (RD) GitHub Governance

## Purpose

This document provides roles, rules, and requirements for users of the Rural Development (RD) GitHub Organization within the United States Department of Agriculture (USDA) GitHub Enterprise Account. In addition, this describes potential use cases for this platform and suggestions for how to successfully collaborate. 

USDA manages a FedRAMP-authorized [GitHub Enterprise Cloud Organization](https://github.com/enterprises/usda-hq) that USDA agencies and mission areas can use to manage source code; establish version control; collaborate on code development; and implement software delivery workflows. USDA agencies and mission areas can create and manage sub-organizations within the USDA GitHub Enterprise Cloud; these sub-organizations can then be used to create and manage repositories for individual applications or projects. RD owns and maintains one such [GitHub Organization](https://github.com/USDA-RD) .

GitHub is a cloud-based platform built on top of Git that allows users to store, share, and work on code. Git is a version control system that tracks changes to code over time. Both have historical ties to software development as tools to effectively collaborate for projects with one or more individuals as they allow for tracking changes to the project over time to mark different versions. They also allow for individual contributors to stay up to date with the work of other contributors on the project, which allows for better development on local machines for individual contributors and reduces frictions related to simultaneously editing code by multiple individuals. While these features are useful for software development workflows, these features have also been found to work well for any projects that require careful tracking or collaborating of text-based inputs that produce some content. This can be code for an application, code to munge data, code for statistical analysis, text for producing a manuscript, or a host of other uses. <https://docs.github.com/en/get-started/start-your-journey/about-github-and-git>

This document assumes the reader has a basic understanding of [Git](https://git-scm.com/docs) and [GitHub](https://docs.github.com/en). It is recommended that individuals requesting access to the [USDA-RD](https://github.com/USDA-RD) GitHub Organization have an intermediate understanding of both Git and GitHub to be a successful collaborator. [AgLearn Percipio]( https://aglearn.percipio.com/) classes are available for individuals to assess their level of understanding of Git and GitHub.

### Exclusions

This document explicitly does not address decisions made by the Office of the Chief Information Officer (OCIO), owners/managers of the USDA GitHub Enterprise, or access / IT support. Changes made by these groups may impact the way that our USDA-RD organization works. 

## [Organization](https://docs.github.com/en/organizations)

Organizations are shared accounts where businesses and open-source projects can collaborate across many projects at once, with sophisticated security and administrative features. [USDA-RD](https://github.com/USDA-RD) is an Organizational Account underneath the [USDA](https://github.com/enterprises/usda-hq) Enterprise Account and USDA-RD must adhere to any restrictions or rules put in place from USDA. Restrictions and rules that are not explicitly defined by the USDA Enterprise Account are at the discretion of USDA-RD and defined within this document.

### Ownership

GitHub [best practices](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/best-practices-for-organizations) suggests Organizations maintain at least two or more owners of the Organization to not have any chokepoints or overreliance on one individual. USDA-RD agrees with this practice and will continue to operate with at least two or more Owners for this Organization. The list of [current owners](https://github.com/orgs/USDA-RD/people?query=role%3Aowner) can be found within the organization’s GitHub page under the People menu. Owners of the Organization will execute administrative issues related to the rest of this document.

## [Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams)

Teams are groups of Organization members that reflect a group's structure with cascading access permissions and mentions. Teams can also nest other Teams within a given Team to create a hierarchical structure. USDA-RD Owners have discretion to create Teams within USDA-RD and will do so adhering to the organizational structure of the Rural Development Mission Area.[DN2.1][SC3.1][RD3.2][SC3.3]

For collaboration across divisions in Rural Development, USDA-RD Owners have the discretion to create unique Teams to facilitate easier collaboration across the entire Organization. This may be appropriate for integrating with platforms such as Databricks for DevOps procedures that involve more than one stakeholder.[SC4.1]

Teams in USDA-RD can be based around a unit, like a division or branch within the RD structure, or around projects. Individuals may be in more than one Team. For example, jon-snow-usda might be in some division where he collaborates on code for data extraction and be in some Team where he collaborates on code for a public facing tool. There are no limits on how many Teams an individual can be included in nor how many Teams can exist within the Organization. However, it is not meaningful to have a Team for every project or repository. If you feel like you need a Team and cannot create it yourself for any reason, request it to an Owner[MM5.1][RD5.2][MM5.3] as outlined for [Becoming a User](#becoming-a-user).

Every Team within the USDA-RD Organization is required to have at least one _Team Maintainer_ with permissions equivalent to Maintain access.

You can find the _Team Maintainer_ within a given Team through the Settings option.

## [Repositories](https://docs.github.com/en/repositories)  

Repositories are the building block of collaboration on GitHub. A repository contains all a project's code, files, and each file's revision history. There is a template repository that contains some very basic files that you may want to reference when you are first getting started.[SC6.1] Teams can discuss and manage their work within a repository by creating issues or using turning on the [Discussions]( https://docs.github.com/en/discussions) feature on GitHub.

Each repository should have a README and a member with Maintain privileges, the repository Maintainer. Do not store any personally identifiable information (PII), application programming interface (API) Keys/Tokens, or secrets[MM7.1][SC7.2] within any repository.

### [Visibility Rules](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams#team-visibility)

Repositories can be designated as Internal, Private, or Public. By default, all repositories in USDA-RD are created as internal repositories that anyone within the Enterprise can access. Sensitive projects or those that are incomplete or meant solely for testing can be designated as private to avoid dissemination across USDA-RD Organization.

It is the responsibility of the repository Maintainer to ensure that there is approval before making a repository public. Maintainers need Enterprise permission in order to make the repository public, so it is unlikely that this will be accidental.

### Workflow Standards

Currently, USDA-RD has no rules around how you structure your workflow. This means that it is left to individual repository Maintainers to maintain Pull Request (PR) review requirements, Continuous Integration (CI) and Continuous Delivery/Deployment (CD) enforcement, commit signing, etc. It is our guidance that individuals that are unfamiliar with CI/CD workflows do not implement these as it is unlikely that an individual would need this sort of workflow if they do not even know what it is doing. See [A beginner’s guide to CI/CD and automation on GitHub]( https://github.blog/developer-skills/github/a-beginners-guide-to-ci-cd-and-automation-on-github/) if you want to know more about these issues. 

By default, Maintainers of a repository are the only ones able to merge a PR. This setting can be adjusted by the Maintainer to allow other users to merge PRs.

PR review requirements, CI/CD enforcement[MM8.1][SC8.2], commit signing, etc. 

## [User Roles](https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization)

From the least access to the most access, the roles for an organization repository are:

- Read: Recommended for non-code contributors who want to view or discuss your project
- Triage: Recommended for contributors who need to proactively manage issues, discussions, and pull requests without write access
- Write: Recommended for contributors who actively push to your project
- Maintain: Recommended for project managers who need to manage the repository without access to sensitive or destructive actions
- Admin: Recommended for people who need full access to the project, including sensitive and destructive actions like managing security or deleting a repository

Principle of least privilege applies: members should only have access necessary for their role and the default for a generic member should be Read Access.

The Owners of USDA-RD will have Admin access.

Teams within USDA-RD must have at least one Maintainer but we recommend at least two Maintainers for the same reasoning as USDA-RD having at least two Owners. Maintainers will have at least Maintain access.

Team Maintainers have discretion to the level they grant users to access repositories within their Team. We suggest the default for users that have access to a Team is to have only Read access.

### Becoming a User

RD staff who want to access the USDA-RD GitHub can submit a request to any Owner to join. Current members may request to add people but should also go through the channel of requesting to an Owner for an individual to join.

Staff must use their USDA email account (@usda.gov) for their GitHub account. Staff should adhere to Enterprise rules regarding GitHub usernames – at least have `-usda` at the end of their username to indicate affiliation with USDA. No GitHub accounts associated with private or personal email addresses will be allowed to access USDA-RD.

Staff are recommended to set up and use two-factor authentication (2FA) to ensure only the intended staff member can access their GitHub account.

### Leaving the Organization

Staff that leave RD will also need to transfer any ownership or maintenance of Repositories and/or Teams within USDA-RD in their off-boarding process. No Repositories or Teams should ever be without a Maintainer.

After leaving RD, former staff will no longer have access to the Organization GitHub.


-->
