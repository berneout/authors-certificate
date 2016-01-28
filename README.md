# The AUTHORS Certificate

A practical approach to code provenance for the GitHub-plus-npm set.

_Under active development. Not yet released for widespread use._

## Inspiration

Inspired by [The Developer Certificate of Origin][DCO] adopted by
Linux kernel developers in the throes of the of the infamous [SCO
suits][SCO].

[DCO]: http://developercertificate.org/

[SCO]: https://en.wikipedia.org/wiki/SCO/Linux_controversies

See also:

[npm's package.json documentation][npm]

> - "contributors": [...]
>
>   If there is an AUTHORS file in the root of your package, npm will
>   treat each line as a Name <email> (url) format, where email and
>   url are optional. Lines which start with a # or are blank, will be
>   ignored.

[npm]: https://docs.npmjs.com/files/package.json#default-values

[The peoplestring-parse package][parse], which parses `AUTHORS`-style
strings with added work-made-for-hire information.

[parse]: https://www.npmjs.com/package/peoplestring-parse

[A pull request to npm's `package.json` normalization routine][PR] to
use peoplestring-parse and friends

[PR]: https://github.com/npm/normalize-package-data/pull/72

## Versioning

The AUTHORS Certificate uses [reviewers editions][reved].

[reved]: https://github.com/kemitchell/reviewers-edition-parse.js
