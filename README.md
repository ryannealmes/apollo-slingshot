# APOLLO SLINGSHOT

This repo is meant get your from setting up your environment to setup environment in 1 command.

```
  docker-compose up
```

What do you get?

## Backend

- graphql setup with basic schema
- es6 code transpiled with webpack
- schema written with `.graphql` files
- automatic server restarts when changes are made
- graphiql exposed on `localhost:3003`

## Front end

- [react-slingshot](https://github.com/coryhouse/react-slingshot) modified to include an apollo client that is connected to your backend
- read the docs for [react-slingshot](https://github.com/coryhouse/react-slingshot) to see everything that's included on the front end - react, redux, reduxdevtools, webpack ...
- apollodevtools

The front and backend are automatically connected. There is an example you should be able to see at `localhost:3000`. This should pull data from the server.

## Setup

If you have docker installed `docker-compose up` should get you going.

If you don't like docker and want to use these repos seperately that's also fine. Docker can be a mouthful to get used to and sometimes it really just gets in the way. If you prefer/don't mind having lots of terminals open you can always just manually start the front and backend. The repos have the instructions you need to get started in both scenarios.

## Future

This is just a start. Some things I think could make this awesome ...

- I think the docker side of things could be improved by mounting volumes instead of building images. This way changes will propagate without builds. Easier for development.
- Include generators to automatically pump out code. In the end it would be great to have something similar to rails where you can spit out scaffolding for most of the repetitive work - creating schemas, connecting to databases, writing migration scripts. 
- Spend time thinking about deploying between environments. Right now the front end caters for developement and production. It would be cool to get the backend doing this as well and allowing the introduction of other environments like staging/UAT.
- I also don't want to limit this to express. It would be great if I could somehow swap in and out different backends - express/hapi/sails/feathers

After working with apollo it feels like it really is a great way to work, but I feel there is a barrier to entry. Setup. Being new in javascript I feel like I experienced this first hand and it sucks. Hopefully this will help and can evolve into something more polished. Let me know your thoughts.
