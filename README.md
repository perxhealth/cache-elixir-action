
![Perx Health](https://user-images.githubusercontent.com/4101096/163123610-9dfa9263-1518-4f5d-8839-9ddc142a513e.png)

# Elixir Setup Action

This repository contains an opinionated **GitHub Action** allowing you to simultaneously
setup a specific version of Elixir and Erlang while also caching your build's
dependencies and compilation. 

## Usage

Add the following `step` to a GitHub Actions workflow.

```yaml
- name: Setup Elixir
  uses: perxhealth/setup-elixir-action@v1
  with:
    otp-version: 25.2.2
    elixir-version: 1.14.3-otp-25
```

### Inputs

The Action currently expects two required inputs.

1. `otp-version`

   the Erlang/OTP version you wish to install, such as `25.2.1`, `26.0.1`, etc.

2. `elixir-version`

   the Elixir version you wish to install, such as `1.14.3`, `1.14.3-otp-25`, etc.

### Outputs

The Action does not currently produce any outputs.

## Development

This is a composite action, so development is limited to and contained with
`action.yaml`. Tweak it to your needs and open a pull request.

### Clone the repository

```bash
$ git clone git@github.com:perxhealth/setup-elixir-action
$ cd setup-elixir-action
```

### Testing

On pushes to any branch, a workflow will run which performs a smoke test on
the action. Once you've made any changes, ensure the workflow located at
`.github/workflows/preflight.yaml` continues to pass.
