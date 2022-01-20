

# NgMfe

This project was generated using [Nx](https://nx.dev).

<p style="text-align: center;"><img src="https://raw.githubusercontent.com/nrwl/nx/master/images/nx-logo.png" width="450"></p>

🔎 **Smart, Fast and Extensible Build System**

## Referemce
https://nx.dev/guides/setup-mfe-with-angular

## Install Nx CLI
npm install -g nx

## Set up a New Nx Workspace
npx create-nx-workspace --preset=empty

## Add the Angular Plugin
npm install --save-dev @nrwl/angular

## Creating our apps (Dashboard & Login)
npx nx g @nrwl/angular:app dashboard --mfe --mfeType=host --routing=true
npx nx g @nrwl/angular:app login --mfe --mfeType=remote --port=4201 --host=dashboard --routing=true

# Creating Shared Libraries
nx g @nrwl/angular:lib shared/data-access-user
nx g @nrwl/angular:service user --project=shared-data-access-user