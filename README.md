Libplanet Explorer Frontend
===========================

[![GitHub Actions Status][github-actions-badge]][github-actions]

This project is a user-facing web app, which renders data provided by
a [Libplanet Explorer server][] instance.

[github-actions-badge]: https://wdp9fww0r9.execute-api.us-west-2.amazonaws.com/production/badge/planetarium/libplanet-explorer-frontend
[github-actions]: https://wdp9fww0r9.execute-api.us-west-2.amazonaws.com/production/results/planetarium/libplanet-explorer-frontend
[Libplanet Explorer server]: https://github.com/planetarium/libplanet-explorer


Development (without server)
----------------------------

First of all, open *.env.development* file and change the value of
`GRAPHQL_ENDPOINT_URI` to refer to our demo server.  The demo server URI can be
found in the first line of *DEPLOYMENTS.tsv*.

And then install dependencies and build the app:

~~~~ bash
npm install
npm run dev
~~~~

You can now see the web app from *localhost:8000*.


Development (with server)
-------------------------

First of all, you need to run the server.  See the below repository and
then follow the instruction in its README:

<https://github.com/planetarium/libplanet-explorer>

If you are sure that your server is ready (check *localhost:5000*)
build the app:

~~~~ bash
npm install
npm run dev
~~~~

You can now see the web app from *localhost:8000*.


Production
----------

Make a *env.production* configuration and then build:

~~~~ bash
{
  echo NETWORK_NAME=example
  echo GRAPHQL_ENDPOINT_URI=https://example.com/graphql/
} > .env.production
npm install
npm run build
~~~~
