# grpc-node-typescript-example
A simple Node application with gRPC communication. Written with Typescript to ensure correct typing in client and server. For simplicity purpose there is only one function `login` shared between client and server.
<br>
Referring to the [link](https://medium.com/@yujso66/%EB%B2%88%EC%97%AD-node-js%EC%97%90%EC%84%9C-grpc-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0-4521604d8852), I attached it with the [original source code](https://github.com/BSalwiczek/grpc-node-typescript-example).

## Running server
```
npx ts-node server.ts
```

## Running client
```
npx ts-node client.ts
```

## Compiling proto file
After any change in `auth.proto` file it needs to be recompiled by running the following command:
```
protoc --plugin=./node_modules/.bin/protoc-gen-ts_proto --ts_proto_out=. ./protos/auth.proto --ts_proto_opt=outputServices=grpc-js,env=node,esModuleInterop=true
```