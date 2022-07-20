# .allstar

OSPO's policies for adherence to security best practices.
[Allstar](https://github.com/ossf/allstar) is a security-policy GitHubApp, that continously monitors organizations for adherence to security best practices, and it is installed in [this organization](https://github.com/kommitters). This repo holds the configuration necessary for all the [policies][policies] with its respective [actions][actions] of allstar in the org.

In the [allstar.yaml][allstar_yaml] file we have the general configuration for allstar, like the strategy to be used, the repos to be included or excluded and some other repo level configurations.

If you need to configure allstar for your own organization you can fork this repo and modify the `yaml` files to match your needs, remember that this repo has to remain with this name `.allstar`, for more information read [Allstar installation][installation_options].

## Policy configuration

The application is running on all the repos of this organization with the `OptOutStrategy` strategy with the following configurations:

### Branch Protection

| Name of setting         | Setting | Description                                                                                                                                                                            |
| ----------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Branches enforced       | Yes     | Enforce upstream branches like `main` `develop` `v*.*` → `v0.1`                                                                                                                        |
| Approval required       | Yes     | If required pull request reviews are enabled on the branch, you won't be able to merge changes into the branch until all requirements in the pull request review policy have been met. |
| Approvals required      | 1       | Approval reviews required to merge changes into a branch.                                                                                                                              |
| Block Force Push        | Yes     | You won't be able to delete or force push to the branch.                                                                                                                               |
| Status check required   | Yes     | If required status checks are enabled on the branch, you won't be able to merge changes into the branch until all of the required CI tests pass.                                       |
| Signed commits required | Yes     | If required commit signing is enabled on a branch, you won't be able to push any commits to the branch that are not signed and verified.                                               |

`Action: issue.`
`Repositories active: all`

### Binary artifacts

* No binary artifacts allowed.

`Action: issue.`
`Repositories active: all`

### Outside collaborators

* Default push access not allowed, only organization members can push directly to the organization repositories.
* Default admin access not allowed.

`Action: issue.`
`Repositories active: all`

### Security

* `SECURITY.md` not empty file required. 

`Action: issue.`
`Repositories active: all`

## Code of conduct
We welcome everyone to contribute. Make sure you have read the [CODE_OF_CONDUCT][coc] before.

## Contributing
For information on how to contribute, please refer to our [CONTRIBUTING][contributing] guide.

## Changelog
Features and bug fixes are listed in the [CHANGELOG][changelog] file.

## License
This library is licensed under an MIT license. See [LICENSE][license] for details.

## Acknowledgements
Made with 💙 by [kommitters Open Source](https://kommit.co)

[actions]: https://github.com/ossf/allstar#actions
[policies]: https://github.com/ossf/allstar#policies
[license]: https://github.com/kommitters/.allstar/blob/main/LICENSE
[coc]: https://github.com/kommitters/.allstar/blob/main/CODE_OF_CONDUCT.md
[changelog]: https://github.com/kommitters/.allstar/blob/main/CHANGELOG.md
[contributing]: https://github.com/kommitters/.allstar/blob/main/CONTRIBUTING.md
[allstar_yaml]: https://github.com/kommitters/.allstar/blob/main/allstar.yaml
[installation_options]: https://github.com/ossf/allstar#installation-options
