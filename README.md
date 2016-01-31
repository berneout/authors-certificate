# The AUTHORS Certificate

Practical provenance for the GitHub-and-npm set

_Under active development. Not yet released for widespread use._

[The AUTHORS Certificate][text] is specially designed for:

1. [open-source][OSI] software projects

2. developed using pull requests, say on [Bitbucket][Bitbucket],
   [GitHub][GitHub], or [GitLab][GitLab]

3. published as [npm][npm] packages

## Use

To use The AUTHORS Certificate:

1. [Read it.][text] Seriously. It's short. And in English.

2. Copy the blank [`AUTHORS` file][AUTHORS] from this repository to
   your project. The file contains only comment lines to start.

3. Copy [`.gitattributes`][gitattributes] to your project. This file
   configures command-line Git to use an alternate merging strategy to
   avoid conflicts between pull requests. Unfortunately, [GitHub's merge
   button does not support `merge=union` attributes][no-merge-union]. If
   you'd like that feature added, [let GitHub know][contact-github].

4. If you use a license, like an MIT- or a BSD-style license, that
   includes a copyright notice at the top, change the notice in your
   `LICENSE` file to something like:

   > Copyright ${year} ${your name} and contributors listed in AUTHORS

   If you use copyright notices in code comments or an Apache-style
   `NOTICE` file, do the same there.

   Make sure you use the right [SPDX expression][SPDX] in the [`license`
   property of your `package.json` file][license-property]. `MIT`,
   `BSD-2-Clause`, and `Apache-2.0` (exact strings) are valid
   expressions for popular license terms on npm.

5. Add your own name to the end of `AUTHORS`.

6. If you have any `contributors` in `package.json`, ask them to read
   `AUTHORS` and send pull requests adding their information.

7. Before merging a pull request from a new contributor, ask them to
   read the `AUTHORS` file and push a commit adding their own
   information to the end of the file. You can bring it in as the
   last commit in their branch. Don't forget to thank them for their
   contribution!

npm will [automatically populate][default-values] the `contributors`
metadata for your package using (non-comment) lines in `AUTHORS`.

## Tools

You can configure your continuous integration server to check `AUTHORS`
for you with [check-authors-certificate][check]:

```shellsession
$ npm install --save-dev check-authors-certificate
```

Then update your `test` npm script in `package.json`:

```json
{
  "scripts": {
    "test": "run your tests && npm run check-authors",
    "check-authors": "check-authors-certificate"
  }
}
```

## Background

The AUTHORS Certificate is heavily inspired by [The Developer
Certificate of Origin][DCO] adopted in Linux kernel development partly
in response to the infamous [SCO Unix copyright lawsuits][SCO]. You can
view an [annotated copy of the Developer of Origin][DCO-ann] among this
project's files.

You may want to read [section 11 of kernel's guide][SubmittingPatches],
[Linus' original proposal][DCO-proposal] for DCO 1.0, and
[kernel trap][kernel trap] on the rationale for new language in DCO 1.1.

The AUTHORS Certificate is useful in four ways:

1. _Helping Folks Take Care of Each Other_. "Provenance" is the fancy legal
   term for "where does this software come from, and do the folks giving
   it away actually have the right to do that?" Provenance has been
   largely ignored outside "enterprisey" foundation projects with form
   contributor license agreements or copyright assignments. With very
   rare exception, [standard open-source licenses don't provide any
   guarantees][Rosen]. That means it's up to contributors to [do their
   homework on concepts like "work made for hire"][WMFH] and practice a
   bit of license hygiene to make sure they aren't creating IP traps for
   folks using their software.

2. _Recordkeeping_. Open-source licensing is about showing users that
   risk to them in using software found online is low. Licenses play a
   part, but so does information about who contributed to a project and
   where to get clarification or reassurance if you need it. Keeping
   good records on that kind of thing is the essence of the Developer
   Certificate of Origin.

3. _Conventions_. The Developer Certificate of Origin is written
   for kernel-style development flow, which is [different from "GitHub
   flow"][Holman]. Kernel development puts rich development process
   metadata in long Git commit messages, and patches are rarely
   committed to history without changes by reviewing maintainers.

4. _Inbound=Outbound_. Both kernel developers and npm package developers
   expect contributors to license their work on the same terms as the
   rest of the project. The Developer Certificate of Origin makes this
   explicit, but also expects per-file license comment headers, which
   aren't the norm on npm. The AUTHORS Certificate also makes licensing
   expectations explicit, but works fine with a package `LICENSE` file
   and metadata in `package.json`.

Overall, you could think of The AUTHORS Certificate as a "port" of The
Developer Certificate of Origin to the prevailing npm development style.

## Versioning

The AUTHORS Certificate uses [reviewers editions][reved].

<!-- Hyperlinks -->
[AUTHORS]: ./AUTHORS
[Bitbucket]: https://bitbucket.com
[DCO]: http://developercertificate.org/
[DCO-ann]: ./DCO-1.1-Annotated.md
[DCO-proposal]: https://lkml.org/lkml/2004/5/23/10
[default-values]: https://docs.npmjs.com/files/package.json#default-values
[GitHub]: https://github.com
[GitLab]: https://gitlab.org
[Holman]: http://zachholman.com/posts/git-commit-history/
[check]: https://www.npmjs.com/packages/check-authors-certificate
[contact-github]: https://github.com/contact
[gitattributes]: ./.gitattributes
[kernel trap]: https://web.archive.org/web/20120409135119/http://kerneltrap.org/node/5277
[license-property]: https://docs.npmjs.com/files/package.json#license
[no-merge-union]: https://github.com/isaacs/github/issues/487
[npm]: https://www.npmjs.com
[OSI]: https://opensource.org
[reved]: https://www.npmjs.com/packages/reviewers-edition-parse
[Rosen]: http://www.rosenlaw.com/html/GL14.pdf
[SCO]: https://en.wikipedia.org/wiki/SCO/Linux_controversies
[SPDX]: https://spdx.org/licenses/
[SubmittingPatches]: https://www.kernel.org/doc/Documentation/SubmittingPatches
[text]: https://github.com/berneout/authors-certificate/blob/master/AUTHORS
[WMFH]: http://worksmadeforhire.com/
