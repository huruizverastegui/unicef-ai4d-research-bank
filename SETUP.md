# Setup

## Custom setup instructions

- Use nvm (node version manager) to install node v18.14.2 (latest stable)
- Activate [corepack to install pnpm](https://pnpm.io/installation#using-corepack)

See example below:

```
nvm install v18.14.2
nvm alias default v18.14.2
which node
corepack enable
corepack prepare pnpm@latest --activate

```

- Install modules in project

```
git clone git@github.com:thinkingmachines/unicef-ai4d-research-bank.git
cd unicef-ai4d-research-bank
pnpm install

```

- Create `.env.local` based from the `.env.sample` file.

- Install a python virtual environment. You can use [virtualenv](https://virtualenv.pypa.io/en/latest/) for this.

- In your virtual environment, run the following command to install the required python libraries

```bash
pip install -r requirements.txt
```

- Make sure to set your virtual environment before running the catalog validation commands

## Customizations

- Deploy to github pages instead of vercel (see [deploy workflow](.github/workflows/deploy.yml))

## Notes

- Using [vite](https://vitejs.dev/) with the [Vitamin template](https://github.com/wtchnm/Vitamin) - an opinionated community template (see [demo site](https://vitamin-wtchnm.vercel.app/))
  - uses [pnpm vs npm](https://pnpm.io/pnpm-vs-npm)
  - uses [vitest](https://vitest.dev/) vs Jest
  - uses husky vs pre-commit
  - ~~uses [commitizen](https://github.com/commitizen/cz-cli) for git-commits~~
  - uses [cypress](https://docs.cypress.io/guides/overview/why-cypress) for e2e (end-to-end) tests
    - note: disabled recording because it requires cypress cloud during CI
  - ~~uses [codecov](https://about.codecov.io/) for code coverage reporting~~
    - for actual repo, will require admin rights to add codecov app to research bank github repo and set repo secret. See [codecov install docs for details](https://docs.codecov.com/docs)
