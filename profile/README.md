<p align="center">
    <a href="https://php-ffi.github.io/docs/"><img src="logo.svg" width="160" height="160" alt="PHP FFI"></a>
</p>

<h1 align="center">PHP FFI</h1>

<p align="center">
    Preprocess and parse C headers, inspect native binaries and locate them on disk — in plain PHP.
</p>

<p align="center">
    <a href="https://php-ffi.github.io/docs/"><b>Documentation</b></a>
    &nbsp;·&nbsp;
    <a href="https://packagist.org/packages/ffi/"><b>Packagist</b></a>
    &nbsp;·&nbsp;
    <a href="https://github.com/orgs/php-ffi/repositories"><b>Repositories</b></a>
</p>

---

A set of independent Composer packages around PHP's
[FFI extension](https://www.php.net/manual/en/book.ffi.php). They cover the
whole path from a C header and a shared library to working FFI bindings:
the header is preprocessed and parsed into an AST, and the library is found
on disk and its exported symbols are read — without a C compiler or any
native tooling. All packages are written in pure PHP and work on Linux,
macOS and Windows.

## Packages

### C headers

- **[ffi/preprocessor](https://github.com/php-ffi/preprocessor)** —
  C23 preprocessor: macros, conditional directives, `#include`.
  The output is what the parser is meant to consume.

  [![Tests](https://github.com/php-ffi/preprocessor/actions/workflows/tests.yml/badge.svg)](https://github.com/php-ffi/preprocessor/actions/workflows/tests.yml)
  [![Version](https://img.shields.io/packagist/v/ffi/preprocessor?label=version)](https://packagist.org/packages/ffi/preprocessor)
  [![PHP](https://img.shields.io/packagist/dependency-v/ffi/preprocessor/php)](https://packagist.org/packages/ffi/preprocessor)

- **[ffi/c-parser](https://github.com/php-ffi/parser)** —
  C23 ([ISO/IEC 9899:2024](https://www.open-std.org/jtc1/sc22/wg14/www/docs/n3220.pdf))
  header parser that produces an AST.

  [![Tests](https://github.com/php-ffi/parser/actions/workflows/tests.yml/badge.svg)](https://github.com/php-ffi/parser/actions/workflows/tests.yml)
  [![Version](https://img.shields.io/packagist/v/ffi/c-parser?label=version)](https://packagist.org/packages/ffi/c-parser)
  [![PHP](https://img.shields.io/packagist/dependency-v/ffi/c-parser/php)](https://packagist.org/packages/ffi/c-parser)

### Binaries

- **[ffi/reflection-library](https://github.com/php-ffi/reflection-library)** —
  reads ELF, PE/COFF and Mach-O binaries: exported and imported symbols.

  [![Tests](https://github.com/php-ffi/reflection-library/actions/workflows/tests.yml/badge.svg)](https://github.com/php-ffi/reflection-library/actions/workflows/tests.yml)
  [![Version](https://img.shields.io/packagist/v/ffi/reflection-library?label=version)](https://packagist.org/packages/ffi/reflection-library)
  [![PHP](https://img.shields.io/packagist/dependency-v/ffi/reflection-library/php)](https://packagist.org/packages/ffi/reflection-library)

- **[ffi/location](https://github.com/php-ffi/location)** —
  resolves the physical path of a binary in the operating system.

  [![Tests](https://github.com/php-ffi/location/actions/workflows/tests.yml/badge.svg)](https://github.com/php-ffi/location/actions/workflows/tests.yml)
  [![Version](https://img.shields.io/packagist/v/ffi/location?label=version)](https://packagist.org/packages/ffi/location)
  [![PHP](https://img.shields.io/packagist/dependency-v/ffi/location/php)](https://packagist.org/packages/ffi/location)

### Runtime

- **[ffi/env](https://github.com/php-ffi/env)** —
  status and availability of the FFI extension in the current environment.

  [![Tests](https://github.com/php-ffi/env/actions/workflows/tests.yml/badge.svg)](https://github.com/php-ffi/env/actions/workflows/tests.yml)
  [![Version](https://img.shields.io/packagist/v/ffi/env?label=version)](https://packagist.org/packages/ffi/env)
  [![PHP](https://img.shields.io/packagist/dependency-v/ffi/env/php)](https://packagist.org/packages/ffi/env)

## Installation

Every package is installed separately with [Composer](https://getcomposer.org):

```sh
composer require ffi/c-parser
```

## Contributing

Bug reports and pull requests are welcome in the repository of the package
they relate to. Please run its test suite (`composer test:unit`) and code
style check (`composer phpcs:check`) before opening a pull request.

## License

All packages are open-source software released under the
[MIT License](https://opensource.org/license/mit).
