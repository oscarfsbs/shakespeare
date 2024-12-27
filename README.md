# shakespeare

[![Package Version](https://img.shields.io/hexpm/v/shakespeare)](https://hex.pm/packages/shakespeare)
[![Hex Docs](https://img.shields.io/badge/hex-docs-ffaff3)](https://hexdocs.pm/shakespeare/)
![Erlang-compatible](https://img.shields.io/badge/target-erlang-b83998)

🎭 General-purpose OTP actors.

## Installation

```sh
gleam add shakespeare
```

```gleam
import gleam/io
import gleam/erlang/process
import shakespeare/actors/periodic

pub fn main() {
  let ping = fn() { io.println("Pong!") }

  periodic.start(do: ping, every: periodic.Ms(1000))

  process.sleep_forever()
}
```
