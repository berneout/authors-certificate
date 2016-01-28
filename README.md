# The AUTHORS Certificate

Practical provenance for the GitHub-and-npm set

_Under active development. Not yet released for widespread use._

## Use Case

The AUTHORS Certificate is specially designed for:

1. open-source software projects

2. developed using pull requests, say on Bitbucket, GitHub, or GitLab

3. published as [npm][npm] packages

To use The AUTHORS Certificate:

1. Read it. Seriously. It's short. And in English.

2. Copy the blank `AUTHORS` file from this repository to your project.
   The file contains only comment lines to start.

3. If you use a license, like an MIT- or a BSD-style license, that
   includes a copyright notice at the top, change the notice in your
   `LICENSE` file to something like:

   > Copyright ${year} ${your name} and contributors listed in AUTHORS

   If you use copyright notices in code comments or an Apache-style
   `NOTICE` file, do the same there.

   Make sure you use the right SPDX expression in the [`license`
   property of your `package.json` file][license-property]. `MIT`,
   `BSD-2-Clause`, and `Apache-2.0` (exact strings) are valid
   expressions for popular license terms on npm.

4. Add your own name to the end of `AUTHORS`.

5. If you have any `contributors` in `package.json`, ask them to read
   `AUTHORS` and send pull requests adding their information.

6. Before merging a pull request from a new contributor, ask them to
   read the `AUTHORS` file and push a commit adding their own
   information to the end of the file. You can bring it in as the
   last commit in their branch. Don't forget to thank them for their
   contribution!

npm will [automatically populate][default-values] the `contributors`
metadata for your package using (non-comment) lines in `AUTHORS`.

[default-values]: https://docs.npmjs.com/files/package.json#default-values

[license-property]: https://docs.npmjs.com/files/package.json#license

[npm]: https://www.npmjs.com

## Background for Developers

The AUTHORS Certificate is heavily inspired by [The Developer
Certificate of Origin][DCO] adopted by Linux kernel developers in the
throes of the of the infamous [SCO suits][SCO].

It's useful in three ways:

1. _Helping people do the right thing_. "Provenance" is the fancy word
   for "where does this software come from, and who has copyright in it?"

2. _Recordkeeping_.

[DCO]: http://developercertificate.org/

[SCO]: https://en.wikipedia.org/wiki/SCO/Linux_controversies

## Inspiration

See also:

[npm's package.json documentation][npm]

> - "contributors": [...]
>
>   If there is an AUTHORS file in the root of your package, npm will
>   treat each line as a Name <email> (url) format, where email and
>   url are optional. Lines which start with a # or are blank, will be
>   ignored.

[The peoplestring-parse package][parse], which parses `AUTHORS`-style
strings with added work-made-for-hire information.

[parse]: https://www.npmjs.com/package/peoplestring-parse

[A pull request to npm's `package.json` normalization routine][PR] to
use peoplestring-parse and friends

[PR]: https://github.com/npm/normalize-package-data/pull/72

## Versioning

The AUTHORS Certificate uses [reviewers editions][reved].

[reved]: https://github.com/kemitchell/reviewers-edition-parse.js
