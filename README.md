# kommitters Security Policies

<img align="right" src="artwork/kommitters_ospo.jpeg"/>
<p>&nbsp;</p>

This repo establishes the kommit's OSPO security policies.

Allstar is a security-policy GitHub app that continuously monitors organizations for adherence to security best practices. Security violations are reported as issues in the affected repositories.

This README.md file describes in detail policies applied to this organization.

To configure Allstar in your organization, fork this repository and modify the `.yaml` files to match your security policies. Visit the [Allstar installation][installation_options] page for more information.

## Policy configuration

The application is running on all the repos of this organization with the `OptOutStrategy` strategy with the following configurations:

### Branch Protection

| Name of setting         | Setting | Description                                                                                                                                                                            |
| ----------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Branches enforced       | Yes     | Enforce upstream branches like `main` `develop` `v*.*` → `v0.1`.                                                                                                                        |
| Approval required       | Yes     | If required pull request reviews are enabled on the branch, you won't be able to merge changes into the branch until all requirements in the pull request review policy have been met. |
| Approvals required      | 1       | Approval reviews required to merge changes into a branch.                                                                                                                              |
| Block Force Push        | Yes     | You won't be able to delete or force push to the branch.                                                                                                                               |
| Status check required   | Yes     | If required status checks are enabled on the branch, you won't be able to merge changes into the branch until all of the required CI tests pass.                                       |
| Signed commits required | Yes     | If required commit signing is enabled on a branch, you won't be able to push any commits to the branch that are not signed and verified.                                               |

`Action: issue`
`Active repositories: public only`

### Binary artifacts

* No binary artifacts allowed.

`Action: issue`
`Active repositories: public only`

### Outside collaborators

* Default push access not allowed, only organization members can push directly to the organization repositories.
* Default admin access not allowed.

`Action: issue`
`Active repositories: public only`

### Security

* `SECURITY.md` not empty file required. 

`Action: issue`
`Active repositories: public only`

---

## Code of conduct
We welcome everyone to contribute. Make sure you have read the [CODE_OF_CONDUCT][coc] before.

## Contributing
For information on how to contribute, please refer to our [CONTRIBUTING][contributing] guide.

## Changelog
Policies changes are listed in the [CHANGELOG][changelog] file.

## License
This repo is licensed under an MIT license. See [LICENSE][license] for details.

## Acknowledgements
The [OpenSSF organization](https://github.com/ossf), and the [Securing Critical Projects Working Group](https://github.com/ossf/wg-securing-critical-projects).

[license]: https://github.com/kommitters/.allstar/blob/main/LICENSE
[coc]: https://github.com/kommitters/.allstar/blob/main/CODE_OF_CONDUCT.md
[changelog]: https://github.com/kommitters/.allstar/blob/main/CHANGELOG.md
[contributing]: https://github.com/kommitters/.allstar/blob/main/CONTRIBUTING.md
[installation_options]: https://github.com/ossf/allstar#installation-options
