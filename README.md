# actions-setup-xcode

<p align="left">
  <a href="https://github.com/sinoru/actions-setup-xcode/actions"><img alt="test status" src="https://github.com/sinoru/actions-setup-xcode/workflows/build-test/badge.svg"></a>

  <a href="https://github.com/sinoru/actions-setup-xcode/actions"><img alt="versions status" src="https://github.com/sinoru/actions-setup-xcode/workflows/xcode-versions/badge.svg"></a>  
</p>


This action sets up a Xcode environment for use in actions by:

- optionally downloading a version of Xcode from Apple Developer. The action will fail if no matching versions are found in local and Apple ID is not available.
- registering problem matchers for error output

# Usage

See [action.yml](action.yml)

Basic:
```yaml
steps:
- uses: actions/checkout@master
- uses: sinoru/actions-setup-xcode@v1.1
  with:
    xcode-version: '11.2.1' # Exact version of a Xcode version to use
    apple-id: 'bot@sinoru.io' # Apple ID to download from Apple Developer when Xcode not available in local
    apple-id-password: ${{ secrets.APPLE_ID_PASSWORD }}
- run: fastlane scan
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)

# Contributions

Contributions are welcome!  See [Contributor's Guide](docs/contributors.md)
