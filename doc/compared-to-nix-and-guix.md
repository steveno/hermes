# Compared to nix and guix

## Philisophical differences

- Hermes has a focus on simplicy and minimalism, while
  attempting to take some the nicest aspects of Nix and guix.
  Hermes provides a fraction of the builtin commands or options.

- Hermes has a focus on allowing you to run everything yourself
  without any need for central infrastructure. Any infrastructure
  we provide is optional, or you can run *easily* on your own.

- Hermes does not place any emphasis on a single blessed package
  tree. Anyone can make their own, Hermes does not come configured
  for one.

## Practical differences

- They are based on a different programming languages, Nix uses a custom
  lazy functional language, Guix uses scheme, and hermes uses
  Janet.

- Arguably a simpler to learn package model. Nix packages are lazy thunks and
  you must program in a lazy functional language.
  Guix packages make use a Scheme DSL, multiple 'strata' of code and 
  a store monad. Hermes packages are just janet functions and when one
  a build gets scheduled, it gets called. All three accomplish more or
  less the same result.

- Both Nix and Guix rely on a build daemon to mediate package
  builds, Hermes uses a setuid binary.

- Hermes has better support for installing software directly from things
  like git repositories hosted online.

- The first package repository for Hermes is based on musl libc.