# SSR example

It is server side rendering example for scala react apps. Because migration to server side rendering sometimes can be long and tricky we had written server side rendering proxy. It can convert almost any scala react app to server side rendered app.

## Required tools

- [docker](https://docs.docker.com/install)
- [docker-compose](https://docs.docker.com/compose/install)

## Running

- run: docker-compose up --build
- https://mapitout.iamsterdam.com/ with server side rendered content will be visible at http://localhost:5050/

## Environment variables

- sourceHost: where original scala react app is hosted
- rootContainer: scala react app root container path
- initPaths: paths where serverside render works, at this moment we are supporting only root path, so it must be ["/"]

## Notes

You must restart proxy when code in source host changed

## Disclaimer

- igeolise/server-side-render:02 docker image is our internal tool
- it is tested and we are using in some sites in production with high load with no problems.
- you can use it free of charge, modify source code, but we are not providing any support and we are not taking any responsibility for it.
