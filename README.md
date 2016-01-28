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

The AUTHORS Certificate is heavily inspired by [The Developer's
Certificate of Origin][DCO] adopted in Linux kernel development partly
in response to the infamous [SCO Unix copyright lawsuits][SCO].

You may want to read [section 11 of kernel's guide][SubmittingPatches],
[Linus' original proposal][DCO-proposal] for DCO 1.0, and
[kernel trap][kernel trap] on the rationale for adding #4 in DCO 1.1.

[DCO-proposal]: https://lkml.org/lkml/2004/5/23/10

[SubmittingPatches]: https://www.kernel.org/doc/Documentation/SubmittingPatches

[SCO]: https://en.wikipedia.org/wiki/SCO/Linux_controversies

[kenel trap]: https://web.archive.org/web/20120409135119/http://kerneltrap.org/node/5277

The AUTHORS Certificate is useful in three ways:

1. _Helping people do the right thing_. "Provenance" is the fancy legal
   term for "where does this software come from, and do the folks giving
   it away actually have the right to do that?" Provenance has been
   largely ignored outside "enterprisey" foundation projects with form
   contributor license agreements or copyright assignments. With very
   rare exception, [standard open-source licenses don't provide any
   guarantees][Rosen].

2. _Recordkeeping_. Open-source licensing is about showing users that
   risk to them in using software found online is low Licenses play a
   part, but so does information about who contributed to a contact, and
   how to contact them. That record keeping value is the essence of the
   Developer's Certificate of Origin.

3. _Conventions_. But the Developer's Certificate of Origin is written
   for the kernel's development style and tooling. Unlike kernel code,
   npm package code is often license-comment-free, with a separate
   `LICENSE` file and `package.json` metadata. Since the Developer's
   Certificate of Origin speaks in terms of licenses in files, it's not
   a match. Moreover, Git's workflow is [different][Holman], placing
   a great deal more development process metadata in long Git commit
   messages, rather than merging commits as first proposed, with
   occasional commit message links to external resources, like issues
   and pull requests. The AUTHORS Certificate accepts that contributors
   will make lightweight commits and rely on Git-external services,
   placing the needed licensing data in a Git-tracked file rather than
   Git history itself.

[DCO]: http://developercertificate.org/

[Holman]: http://zachholman.com/posts/git-commit-history/

[Rose]: http://www.rosenlaw.com/html/GL14.pdf

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
