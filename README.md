# OpenOdin Server

Run a general OpenOdin server.

In OpenOdin's proper terminology this is a `service`, which is also just a peer.

We do, however, use classic terminology (like "servers") when we are talking about a peer with the specific role of being a central peer between other peers.

Do not let the old terminology worry you. This "server" can easily be run in a redundant way to not have it being a single point of failure, or even run it without a single point of authority to not be in the hands of a single authority over the servers.

This repo does not contain any code, because no code is needed for many use cases. It does however come with two JSON configuration files which are the important parts.

## Setup

```sh
git clone https://github.com/OpenOdin/server

cd server

npm i
```

Create a keypair for the server:  
```sh
npm run keygen
```

The keypair is saved in the root directory named `keyfile.json`.  
**Do NOT** add this file to the git repo.

Configure `./conf/server.json` and `./conf/wallet.json` if needed. Its default configuraion is to listen at port `1117` and allow any public key and IP to connect.

The storage is configured to use _SQLite_ and the data is stored in the `data` dir.
**Do NOT** add this directory to the git repo.

## Run Server

```sh
npm run server
```
