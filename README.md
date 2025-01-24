# OrbitDBSetup

## Connecting peer 2 to peer 1

Launch peer 1 from the terminal:

```bash
node test.js
```

Once launched you will see some output which may look something like this:

```
libp2p address (copy one of these addresses then dial into this node from the second node) [
  Multiaddr(/ip4/127.0.0.1/tcp/36161/p2p/12D3KooWKFWB78Hka2uPVNYYoXfucWp6rDLsQzr5CFiP67NAo7YF),
  Multiaddr(/ip4/192.168.1.22/tcp/36161/p2p/12D3KooWKFWB78Hka2uPVNYYoXfucWp6rDLsQzr5CFiP67NAo7YF),
  Multiaddr(/ip4/100.64.100.6/tcp/36161/p2p/12D3KooWKFWB78Hka2uPVNYYoXfucWp6rDLsQzr5CFiP67NAo7YF)
]
my-db address (copy my db address and use when launching peer 2) /orbitdb/zdpuB2aYUCnZ7YUBrDkCWpRLQ8ieUbqJEVRZEd5aDhJBDpBqj
```

It contains the libp2p address and db address. You will need both of these when connecting from peer 2.

Open another terminal and launch peer 2. The command takes the form `node test.js <orbitdb-address> <libp2p-address>`

```bash
node test.js /orbitdb/zdpuB2aYUCnZ7YUBrDkCWpRLQ8ieUbqJEVRZEd5aDhJBDpBqj /ip4/127.0.0.1/tcp/36161/p2p/12D3KooWKFWB78Hka2uPVNYYoXfucWp6rDLsQzr5CFiP67NAo7YF
```

What is happening is the second peer is dialing the first peer on the /ip4/ address then opens the database.
