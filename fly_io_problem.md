## Problems connectiong to Fly.io

In some cases (the cause is so far unknown) running Fly.io especially on Windows WSL has caused problems. If the following command just hangs

```bash
flyctl ping -o personal
```

your computer can not for some reason connect to Fly.io

If you run to this problem, you might try [GitHub Actions](https://fly.io/docs/app-guides/continuous-deployment-with-github-actions/), (that is the topic of the [part 11](https://fullstackopen.com/en/part11) of this course). With GitHub actions you can ask GitHub to deploy the app to the Fly.io.

The steps to setup GitHub Actions for your project are followng:

- Delete your current (non-functioning) apps on fly.io in your dashboard https://fly.io/dashboard
- Create a secret key in fly at https://fly.io/user/personal_access_tokens and hold on to it
- Go to your github repo `https://github.com/<yourGitAccount>/<yourRepoName>/settings` , head to 'Secrets ' => 'Actions', and then create a repo secret key `FLY_API_TOKEN` with the secret key in the previous step
- Reclone your repo so that you have an updated repo locally (you can delete the old files before recloning)
- Edit .gitignore and remove `fly.toml`. This file will need to be pushed into the repository to allow deployment to happen
- `fly auth login` in your terminal to make sure you're authenticated, then run `fly launch` to create new app in your root directory, but choose **not** to deploy - this will generate a new `fly.toml` file - double check this file has `app = "<your app name>"` to make sure it's pointing to the correctly named app seen on your dashboard
- Create a new directory tree from the root directory leading to a main.yml file -  .github/workflows/main.yml with these contents:

```yml
name: Fly Deploy
on: [push]
env:
  FLY_API_TOKEN: ${{ secrets.FLY_API_TOKEN }}
jobs:
  deploy:
      name: Deploy app
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v2
        - uses: superfly/flyctl-actions/setup-flyctl@master
        - run: flyctl deploy --remote-only
```
  
.yml file is used by GitHub Actions to run each command and deploy your app onto the fly server, and Actions will use the API token we created in step (3) 

- Commit your now-updated repo with all these changes (`git add .`,  `git commit -m "<commit msg>"`, `git push`)
- You can head to `https://github.com/<yourGitAccount>/<yourRepoName>/actions` and see github Actions in-progress; your app will be deploy if everything checks out
- Now whenever there is a new commit, Github Actions will redeploy your app automatically! You can read more about this github feature [here](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions#create-an-example-workflow).
- If on future commits the react app on Fly.io shows a blank screen with an error 404 for a `.js` build file, try to `ctrl-F5` / clean-reload the tab to clear cache - if you think fly.io app isn't up to date, you can rerun a Github Action: head to the Actions tab, click on the most recent workflow runs, then the button _rerun all jobs_.

Big thanks [Leon Poon](https://github.com/Sheceido) for writing this!
