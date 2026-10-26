# Release boundary

NERP's private source owner maintains `distribution/product.json` and its schema.
Build and test there; this public repository only distributes accepted artifacts.

Before transfer, verify the exact source/version/build identity, all seven
product binaries, embedded Vite assets, complete dependency licenses/notices,
checksums, synthetic clean launch, update and rollback. Real customer data,
credentials and private build logs must never be included. Contract use rights
remain separate from public download access.

Use an immutable `vX.Y.Z` tag of this public repository's reviewed metadata
snapshot. Never push private source commits, branches or tags here. Transfer
only the complete accepted archive, reviewed public release-manifest.json and
SHA256SUMS into one draft release. Read all draft assets back and verify their
exact identities before promotion. Existing maintainer authentication performs
the explicit cross-repository transfer; this setup creates no persistent token
or new CI secret. An ordinary private-repository GITHUB_TOKEN is not assumed
to authorize writes here.

Publish a complete accepted stable version, then independently download it
without authentication and verify all asset hashes and declared contents.
Record the tested platform and acceptance scope in the public version record.
Do not claim unsigned hashes are an independent signing identity or that the
public repository built the private product. Establish any signing authority
explicitly before claiming signed provenance.

Never replace published bytes under the same version. Fixes receive a new tag.
Prereleases do not replace the stable channel. Binary acceptance/publication
remains private-owner issue #53 until every required check passes. The public
repository may exist without an official release during that work.
