# [Valheim]

![Rust Build](https://github.com/mbround18/valheim-docker/workflows/Rust/badge.svg)
![Docker Build](https://github.com/mbround18/valheim-docker/workflows/Docker/badge.svg)


## Docker

### Docker Compose

```yaml
services:
  valheim:
    image: mbround18/valheim:latest
    ports:
      - 2456:2456/udp
      - 2457:2457/udp
      - 2458:2458/udp
    env:
      NAME: "Valheim Docker"
      WORLD: "Dedicated"
      PORT: "2456"
      PASSWORD: "something-secret"
    volumes:
    - ./valheim:/home/steam/valheim
```

## Odin

> Odin relies on Rust. [Please install Rust](https://www.rust-lang.org/tools/install)
>
> Odin also assumes that you have SteamCMD already installed. [Install instructions for SteamCMD.](https://developer.valvesoftware.com/wiki/SteamCMD)
>
> Odin is designed to be cross-platform using Rust as its builder.
> If you have the proper build tools installed you should be able to run Odin on any system.
> Current Supported Architecture: Unix & Linux based systems. Windows coming soon.

Odin is a CLI tool utilized for installing, starting, and stopping [Valheim] servers


### Installation

```sh
cargo install --git https://github.com/mbround18/valheim-docker
```

### Usage

![usage menu](./docs/assets/main-menu.png)

#### Install Valheim

```sh
odin install
```

#### Start Valheim

```sh
odin start
```

![start menu](./docs/assets/start-menu.png)
#### Stop Valheim

```sh
odin stop
```


[Valheim]: https://www.valheimgame.com/
