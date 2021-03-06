## sewer, the ACME library and command-line client

This is a quick & dirty directory of the docs directory, which is still a
work in progress - in particular, some of the files are not yet properly
linked from the README or other docs.  There's some overlap and redundancy,
and doubtless some out of date bits.  The _internals_ documents include some
that were written more as technical essays when I was sorting out some
issue, and those may not have been updated since before the features were
implemented.

### General and "user" docs.

- [README](https://github.com/komuw/sewer) and project page.
- [CHANGELOG](CHANGELOG) with links to per-release notes when they exist
- [sewer-cli](sewer-cli) Documentation for the command line tool

### Internals (docs for direct users of Client, etc.)

- [sewer-as-a-library](sewer-as-a-library) Rewritten _Usage_ section from
  README using new interfaces, etc.  WIP.

- [Aliasing.md](Aliasing), just renamed from DNS-Aliasing, so the contents must
  still be in flux, too.  Probably a lumpy blending of implementation and
  user notes, still.
- [catalog](catalog) the driver catalog and support in catalog.py
- [dns-01](dns-01) sewer's existing (legacy) DNS providers as well as some
  skeleton code for implementing a new-model driver
- [DNS-Propagation.md](DNS-Propagation) has become (is becoming?) the document
  about _what_ propagation means to the ACME process and _how_ we might
  manage it.  From the title you can tell it began when I was still thinking
  of propagation as DNS thing.
- [http-01](http-01) guide for writing HTTP driver  **TO DO**
- [LegacyDNS.md](LegacyDNS) Documents the new-model shim (still named
  BaseDNS) that allows unmigrated Legacy DNS drivers to continue working. 
  Authors of any DNS module, Legacy or new, should review this... and,
  hopefully, migrate to or start anew as new-model Providers.
- [UnifiedProvider.md](UnifiedProvider) was the first intentional thought
  doc.  It has been written and revised repeatedly since Alec's original
  http-01 changes got me thinking about how best to accomodate both, as well
  as other validation methods that were already RFCs or on their way.
- [unpropagated.md](unpropagated) was the first separate piece.  Begun as I was
  figuring out what to do, and changes upon changes here as well.  Heading
  towards being documentation of the implementation.
- [wildcards.md](wildcards) Notes about wildcard certificates - they should
  work for all drivers now! - and a special case where there are probably
  still issues.

- [ACME](ACME) A bit of history, a start on a technical essay, or ??? 
  Notes on various things related to ACME and Let's Encrypt's servers.
