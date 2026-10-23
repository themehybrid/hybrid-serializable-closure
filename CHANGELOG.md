# Change Log

You can see the changes made via the [commit log](https://github.com/themehybrid/hybrid-serializable-closure/commits/main) for the latest release.

## [1.0.0] - 2026-10-23

### Added

- Launch, ported from laravel/serializable-closure 2.0.13.
- The upstream test suite, ported to `qa/`, a separate Composer project
  because Pest 5 needs PHP 8.4. Run with `composer test`.

### Fixed

- Unserializing a closure failed: the stream protocol
  `hybrid_core-serializable-closure` was rejected by
  `stream_wrapper_register()`, because a scheme cannot contain `_`. It is now
  `hybrid-serializable-closure`.
- The package did not parse on PHP 8.2: it declared typed class constants,
  which need PHP 8.3.
