# Example - commitizen and standard-version

## Setup

```bash
npm install
npm start # demonstration
```

## How to commit and push changes

This repository _enforces_ the user to enter a properly formatted commit message
via commitizen. You do not have to do anything different than `git commit` when
commiting changes.

Once you have finished the commitizen dialog, you can easily push changes with
`git push`.

## How to release and later publish the package

This package uses [standard-version](https://github.com/conventional-changelog/standard-version)
and [commitizen](https://github.com/commitizen/cz-cli) for standardizing commit
messages, releasing tags and updating the changelog.

When you're ready to release, execute the following commands in the given order:

1. `git checkout master`
2. `git pull origin master`
3. `npm run release -- --no-verify` (or `npx standard-version --no-verify`)
4. `git push --follow-tags origin master`

Now you are ready to publish the package with: `npm publish`

## License

[MIT](LICENSE)
