# Changelog

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.2] - 2018-07-12 <a name="1.1.2"></a>
### Fixed
- Fixed compilation error in 1.1.1 on rustc < 1.27, now compiles again on rustc >= 1.10. Fixes [#11].

## [1.1.1] - 2018-06-24 - **Yanked** <a name="1.1.1"></a>
### ***Yanked***
*Not recommended due to introducing compilation error on rustc versions prior to 1.27.*
### Fixed
- Fix subnormal float conversions when `use-intrinsics` is not enabled. By [@Moongoodboy-K].

## [1.1.0] - 2018-03-17 <a name="1.1.0"></a>
### Added
- Made `to_f32` and `to_f64` public. Fixes [#7], by [@PSeitz].

## [1.0.2] - 2018-01-12 <a name="1.0.2"></a>
### Changed
- Update behavior of `is_sign_positive` and `is_sign_negative` to match the IEEE754 conforming
behavior of the standard library since Rust 1.20.0. Fixes [#3], by [@tspiteri].
- Small optimization on `is_nan` and `is_infinite` from [@tspiteri].
### Fixed
- Fix comparisons of +0 to -0 and comparisons involving negative numbers. Fixes [#2], by [@tspiteri].
- Fix loss of sign when converting `f16` and `f32` to `f16`, and case where `f64` NaN could be
converted to `f16` infinity instead of NaN. Fixes [#5], by [@tspiteri].

## [1.0.1] - 2017-08-30 <a name="1.0.1"></a>
### Added
- More README documentation.
- Badges and categories in crate metadata.
### Changed
- `serde` dependency updated to 1.0 stable.
- Writing changelog manually.

## [1.0.0] - 2017-02-03 <a name="1.0.0"></a>
### Added
- Update to `serde` 0.9 and stable Rust 1.15 for `serialize` feature.

## [0.1.1] - 2017-01-08 <a name="0.1.1"></a>
### Added
- Add `serde` support under new `serialize` feature.
### Changed
- Use `no_std` for crate by default.

## 0.1.0 - 2016-03-17 <a name="0.1.0"></a>
### Added
- Initial release of `f16` type.

[#2]: https://github.com/starkat99/half-rs/issues/2
[#3]: https://github.com/starkat99/half-rs/issues/3
[#5]: https://github.com/starkat99/half-rs/issues/5
[#7]: https://github.com/starkat99/half-rs/issues/7
[#11]: https://github.com/starkat99/half-rs/issues/11

[@tspiteri]: https://github.com/tspiteri
[@PSeitz]: https://github.com/PSeitz
[@Moongoodboy-K]: https://github.com/Moongoodboy-K

[Unreleased]: https://github.com/starkat99/half-rs/compare/v1.1.2...HEAD
[1.1.2]: https://github.com/starkat99/half-rs/compare/v1.1.1...v1.1.2
[1.1.1]: https://github.com/starkat99/half-rs/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/starkat99/half-rs/compare/v1.0.2...v1.1.0
[1.0.2]: https://github.com/starkat99/half-rs/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/starkat99/half-rs/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/starkat99/half-rs/compare/v0.1.1...v1.0.0
[0.1.1]: https://github.com/starkat99/half-rs/compare/v0.1.0...v0.1.1