# homebrew-norns

Homebrew formulae for the [SRE-Norns](https://github.com/sre-norns) command-line
tools, on macOS and Linux, amd64 and arm64.

## How do I install these formulae?

`brew install sre-norns/norns/<formula>`

Or `brew tap sre-norns/norns` and then `brew install <formula>`.

Or, in a [`brew bundle`](https://github.com/Homebrew/homebrew-bundle) `Brewfile`:

```ruby
tap "sre-norns/norns"
brew "<formula>"
```

## Formulae

| Formula | What | Source |
|---|---|---|
| `urthctl` | Command-line client for [Urth](https://github.com/sre-norns/urth) synthetic monitoring | [sre-norns/urth](https://github.com/sre-norns/urth) |
| `expbctl` | Command-line client for [Exp-Bench](https://github.com/sre-norns/exp-bench); arrives once that repository is public | [sre-norns/exp-bench](https://github.com/sre-norns/exp-bench) |

The formulae install each product's published release archives; nothing is
built from source. They are generated: each product renders its formula with
`scripts/homebrew-formula.py`, and its `Homebrew tap` workflow opens a pull
request here for every stable release. Change the template in the product
repository, not the formula here, which the next release overwrites.

Every pull request runs `brew test-bot`, which audits, installs and tests the
changed formulae on macOS (Apple silicon and Intel) and Linux.

## Documentation

`brew help`, `man brew` or check [Homebrew's documentation](https://docs.brew.sh).
