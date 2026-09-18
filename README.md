# Blue-talk

A decentralized, multi-hop mesh messaging and file-transfer network built in Go.

Blue-talk lets devices discover each other and exchange messages and files over
Bluetooth and local Wi-Fi, without requiring internet access or a central
server. Messages can hop across intermediate devices to reach a destination
that isn't directly reachable, similar in spirit to a mesh network.

## Core ideas

- **Nodes** — every device running Blue-talk is a node with its own identity
- **Discovery** — nodes find each other on the local network (later: Bluetooth/Wi-Fi Direct)
- **Multi-hop routing** — messages can travel through intermediate nodes to reach a destination
- **Store & forward** — nodes hold messages for peers that are temporarily unreachable
- **Fault tolerance** — if a node drops out, the network finds another route
- **End-to-end encryption** — intermediate nodes forward messages without reading their contents
- **Optional supernode** — an Ubuntu server can provide coordination, storage, and monitoring, but the network keeps working without it

## Status

Early development. Currently working through the foundational networking stages
before adding Bluetooth/Wi-Fi transports.

See `PROJECT_STRUCTURE.Rmd` for the full technical breakdown, stack, and
development roadmap.

## Requirements (current stage)

- Go (version TBD — will pin once the module is initialized)
- No external hardware required yet — development happens over local TCP/UDP

## Getting started

Coming soon — the first working piece is a two-node TCP handshake using a
shared JSON message format.

## License

TBD