> **⚠️ Note:** To use this GitHub Action, you must have access to GitHub Actions. GitHub Actions are currently only available in public beta. You can [apply for Github Actions beta access here](https://github.com/features/actions).

# ApiGen - ***Github Action***
Github Action To Generate Code Docs Website For PHP Using ApiGen

## Configuration
| Argument | Default | Description |
| --- | ------- | ----------- |
|`push_to_branch` | gh-pages | Which Branch To Push |
|`before_cmd` | null | Option to run custom cmd before generating docs |
|`after_cmd` | null | Option to run custom cmd after generating docs |
---

> **Note** Provide A Branch Which is only for the docs. if any other contents in it then all will be deleted **DO NOT USE : MASTER**  


## Example Workflow File
```yaml
name: ApiGen

on: [push]

jobs:
  apigen:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - name: ApiGen Docs Generator
      uses: varunsridharan/action-apigen@master
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        
```

---

## Contribute
If you would like to help, please take a look at the list of
[issues][issues] or the [To Do](#-todo) checklist.

## License
Our GitHub Actions are available for use and remix under the MIT license.

## Copyright
2017 - 2018 Varun Sridharan, [varunsridharan.in][website]

If you find it useful, let me know :wink:

You can contact me on [Twitter][twitter] or through my [email][email].

## Backed By
| [![DigitalOcean][do-image]][do-ref] | [![JetBrains][jb-image]][jb-ref] |  [![Tidio Chat][tidio-image]][tidio-ref] |
| --- | --- | --- |

[twitter]: https://twitter.com/varunsridharan2
[email]: mailto:varunsridharan23@gmail.com
[website]: https://varunsridharan.in
[issues]: issues/

[do-image]: https://vsp.ams3.cdn.digitaloceanspaces.com/cdn/DO_Logo_Horizontal_Blue-small.png
[jb-image]: https://vsp.ams3.cdn.digitaloceanspaces.com/cdn/phpstorm-small.png?v3
[tidio-image]: https://vsp.ams3.cdn.digitaloceanspaces.com/cdn/tidiochat-small.png
[do-ref]: https://s.svarun.in/Ef
[jb-ref]: https://www.jetbrains.com
[tidio-ref]: https://tidiochat.com

