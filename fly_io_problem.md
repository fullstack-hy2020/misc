## Problems connectiong to Fly.io

In some cases (the cause is so far unknown) running Fly.io especially on Windows WSL has caused problems. If the following command just hangs

```bash
flyctl ping -o personal
```

your computer can not for some reason connect to Fly.io

If you run to this problem, you might try [GitHub Actions](https://fly.io/docs/app-guides/continuous-deployment-with-github-actions/), (that is the topic of the [part 11](https://fullstackopen.com/en/part11) of this course). With GitHub actions you can ask GitHub to deploy the app to the Fly.io.

The steps to setup GitHub Actions for your project are followng:

- delete your current (non-functioning) apps on fly.io in your dashboard https://fly.io/dashboard
- create a secret key in fly and save it somewhere https://fly.io/user/personal_access_tokens
- go to your github repo https://github.com/<yourGitAccount>/<yourRepoName>/settings , head to 'Secrets ' => 'Actions', and then create a repo secret key FLY_API_TOKEN 
- reclone your repo so that you have an updated repo locally (you can delete the old files before recloning)
- Edit .gitignore and remove fly.toml. This file will need to be pushed into the repository to allow deployment to happen.
- Run flyctl apps create to create a fly.toml file (this will create a new app in your dashboard... remember to fly auth login to make sure you're authenticated) 
(you can double check your fly.toml file has app = "<your app name on the dashboard>" to make sure it's pointing to the correct app)
- Create a new directory tree from the root directory leading to a main.yml file::  .github/workflows/main.yml with these contents: 

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
  
.yml file is used by GitHub Actions to run each command and deploy your app onto the fly server, making sure to use the API token we created in step (3) 

- commit your now updated repo with all these changes (git add .,  git commit -m "<commit msg>", git push)
- now you can head to `https://github.com/<yourGitAccount>/<yourRepoName>/actions` and see the progress, if everything goes well, your app will be deployed
-- I had an issue with flyctl apps create where it did not recreate a .toml file - you can either use an old .toml file but just edit the app = ... to have the same name as the app created on the fly dashboard, or do another fly launch, but just don't deploy directly from the CLI
