# monorepo for the decentralized oracle UI's

currently published on [https://decentralized-oracle.substrate.fi](https://decentralized-oracle.substrate.fi)

## build

to build the Global UI:

* clone this repo

```
git clone git@github.com:decentralized-oracles/ui-monorepo.git
```

* inside the ui-monorepo folder, clone the 4 UI repo

```
cd ui-monorepo
git clone git@github.com:decentralized-oracles/ui-home.git
git clone git@github.com:decentralized-oracles/graph-api-ui.git
git clone git@github.com:decentralized-oracles/price-feed-ui.git
git clone git@github.com:decentralized-oracles/vrf-ui.git
```

* inside each directory, execute the `yarn build` command

```
cd ui-home && yarn build && cd ..
cd graph-api-ui && yarn build && cd ..
cd price-feed-ui && yarn build && cd ..
cd vrf-ui && yarn build && cd ..
```

the global site will be generated into `/dist` directory

the `/dist/assets` folder will not be purged if you build again the `ui-home` site
to cleanup unused files, you need to manually delete the `/dist/assets` folder content before building the `ui-home` site

## Deploy.yml

setup the variables on Github to use the deploy feature

* WEBSITE_UUID : copy UUID from hosting bucket on Apillon dashboard
* APILLON_API_KEY : your previously created API key
* APILLON_API_SECRET : your previously created API secret
