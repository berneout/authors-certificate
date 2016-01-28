# The AUTHORS Certificate

Practical provenance for the GitHub-and-npm set

_Under active development. Not yet released for widespread use._

## Use

[The AUTHORS Certificate][text] is specially designed for:

1. [open-source][OSI] software projects

2. developed using pull requests, say on [Bitbucket][Bitbucket],
   [GitHub][GitHub], or [GitLab][GitLab]

3. published as [npm][npm] packages

[Bitbucket]: https://bitbucket.com

[GitHub]: https://github.com

[GitLab]: https://gitlab.org

[OSI]: https://opensource.org

[text]: https://github.com/berneout/authors-certificate/blob/master/AUTHORS

To use The AUTHORS Certificate:

1. [Read it.][text] Seriously. It's short. And in English.

2. Copy the blank `AUTHORS` file from this repository to your project.
   The file contains only comment lines to start.

3. If you use a license, like an MIT- or a BSD-style license, that
   includes a copyright notice at the top, change the notice in your
   `LICENSE` file to something like:

   > Copyright ${year} ${your name} and contributors listed in AUTHORS

   If you use copyright notices in code comments or an Apache-style
   `NOTICE` file, do the same there.

   Make sure you use the right [SPDX expression][SPDX] in the [`license`
   property of your `package.json` file][license-property]. `MIT`,
   `BSD-2-Clause`, and `Apache-2.0` (exact strings) are valid
   expressions for popular license terms on npm.

4. Add your own name to the end of `AUTHORS`.

5. If you have any `contributors` in `package.json`, ask them to read
   `AUTHORS` and send pull requests adding their information.

6. Before merging a pull request from a new contributor, ask them to
   read the `AUTHORS` file and send a pull request adding their own
   information to the end of the file. You can bring it in as the
   last commit in their branch. Don't forget to thank them for their
   contribution!

npm will [automatically populate][default-values] the `contributors`
metadata for your package using (non-comment) lines in `AUTHORS`.

[SPDX]: https://spdx.org/licenses/

[default-values]: https://docs.npmjs.com/files/package.json#default-values

[license-property]: https://docs.npmjs.com/files/package.json#license

[npm]: https://www.npmjs.com

## Background

The AUTHORS Certificate is heavily inspired by [The Developer
Certificate of Origin][DCO] adopted in Linux kernel development partly
in response to the infamous [SCO Unix copyright lawsuits][SCO].

You may want to read [section 11 of kernel's guide][SubmittingPatches],
[Linus' original proposal][DCO-proposal] for DCO 1.0, and
[kernel trap][kernel trap] on the rationale for new language in DCO 1.1.

[DCO-proposal]: https://lkml.org/lkml/2004/5/23/10

[SubmittingPatches]: https://www.kernel.org/doc/Documentation/SubmittingPatches

[SCO]: https://en.wikipedia.org/wiki/SCO/Linux_controversies

[kernel trap]: https://web.archive.org/web/20120409135119/http://kerneltrap.org/node/5277

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

[DCO]: http://developercertificate.org/

[Holman]: http://zachholman.com/posts/git-commit-history/

[Rosen]: http://www.rosenlaw.com/html/GL14.pdf

[WMFH]: http://worksmadeforhire.com/

## Versioning

The AUTHORS Certificate uses [reviewers editions][reved].

[reved]: https://github.com/kemitchell/reviewers-edition-parse.js
