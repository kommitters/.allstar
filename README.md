# .allstar

OSPO's policies for adherence to security best practices.
[Allstar](https://github.com/ossf/allstar) is a security-policy GitHubApp, that continously monitors organizations for adherence to security best practices, and it is installed in [this organization](https://github.com/kommitters). This repo holds the configuration necessary for all the [policies](https://github.com/ossf/allstar#policies) with its respective [actions][actions] of allstar in the org.

## Policy configuration

The application is running on all the repos of this organization with the `OptOutStrategy` strategy with the following configurations:

### Branch Protection

| Name of setting         | Setting |
| ----------------------- | ------- |
| Branches enforced       | Yes     |
| Approval required       | Yes     |
| Approvals required      | 1       |
| Block Force Push        | Yes     |
| Signed commits required | Yes     |
| Status check required   | Yes     |

`Action: issue.`
`Repositories active: all`

### Binary artifacts

* No binary artifacts allowed

`Action: issue.`
`Repositories active: all`

### Outside collaborators

* Default push access allowed.
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
