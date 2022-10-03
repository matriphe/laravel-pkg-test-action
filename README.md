# Laravel Package Test Action

GitHub Action to test Laravel package and library compatibility using PHPUnit.

## Usage

This action will automatically check out your code.

```yaml
steps:
  - uses: matriphe/laravel-pkg-test-action@v2
    with:
      operating_system: ubuntu-latest # The Operating System where the test runs
      php_version: 8.1 # The PHP version where the test runs
      php_extensions: pdo_sqlite,sqlite3 # The PHP extension enabled for the test, separated by comma
      laravel_version: 9.* # The Laravel framework version where the test runs
      branch: main # The branch name, tag name, or git reference checksum to check out
      laravel_install_args: --prefer-dist # The arguments passed to Composer when installing Laravel framework
      package_install_args: --prefer-dist --no-progress  # The arguments passed to Composer when installing the package
      phpunit_args: --filter some_test # The arguments passed to PHPUnit when running the test
      shell_name: bash # The shell name used to run the test
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).