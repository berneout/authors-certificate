> Developer Certificate of Origin
> Version 1.1
>
> Copyright (C) 2004, 2006 The Linux Foundation and its contributors.
> 660 York Street, Suite 102,
> San Francisco, CA 94110 USA
>
> Everyone is permitted to copy and distribute verbatim copies of this
> license document, but changing it is not allowed.

The DCO includes its license in its text.

The AUTHORS Certificate provides its license in a separate `LICENSE`
file, and does not require reproduction of its copyright notice or
license terms with the text of the AUTHORS Certificate itself.

> Developer's Certificate of Origin 1.1
>
> By making a contribution to this project, I certify that:

Using "making a contribution" as the trigger is a bit more general. The
AUTHORS Certificate trades away that flexibility for certainty: Those
who add themselves to `AUTHORS` in a commit make the certifications
listed. That certainty, plus Git Flow, add up to pretty good evidence of
intent, at the moment a developer's name was written in `AUTHORS`, that
looks a lot more like signature than back-and-forth in a mailing list
discussing a patch.

> (a) The contribution was created in whole or in part by me and I
>     have the right to submit it under the open source license
>     indicated in the file; or

Unlike the DCO, the AUTHORS Certificate requires contributions be
_entirely_ original work of the submitting contributor. If a pull
request comes in with commits from multiple authors, all authors should
be called on to push separate commit appending their info to AUTHORS.

As a practical matter, "found" code is highly unlikely to have rigorous
provenance information. Writing contributions oneself is the cleanest,
most direct route to avoiding provenance issues, though there is
always a possibility that someone will lift code from another without
permission and try to pass it off as original.

The language "and I have the right..." speaks to provenance for works
made for hire, but doesn't provide any hint that developers should
consider whether they may not have such rights for their own work. The
AUTHORS Certificate addresses more directly by requesting different
information be added to AUTHORS if the developer's practical situation
includes facts that tend to show work made for hire might be an issue.
It requires that authors certify a legal conclusions only when they
claim that work made for hire is not an issue. When developers list a
work-for entity in AUTHORS, they merely certify the facts that they
have a relationship about intellectual property and have received
prophylactic permission to publish contributions. This latter option
does not include any certification of any legal conclusion.

> (b) The contribution is based upon previous work that, to the best
>     of my knowledge, is covered under an appropriate open source
>     license and I have the right under that license to submit that
>     work with modifications, whether created in whole or in part
>     by me, [...]

Again, the AUTHORS Certificate requires certification that contributions
are original work.

This reflects a somewhat more basic difference between Kernel Flow
and GitHub Flow. DCO is partially concerned about code provenance for
code that comes in from outside the kernel project, but also mightily
concerned with how that code then bounces around among kernel subsystem
and other maintainers, gathering sign-offs until it is eventually merged
into Linus' branch.

GitHub flow is much more direct, in that the outside authors of new
patches routinely interact directly with the maintainer who will
eventually merge. Back-and-forth happens in an external system, like
GitHub comments. If maintainers feed back requests to change the patch,
these changes are as often made by the pull request author pushing
amendments.

>      [...] under the same open source license (unless I am
>     permitted to submit under a different license), [...]

This is where DCO address inbound=outbound licensing. The AUTHORS
Certificate formalizes the same convention.

>                                               [...] as indicated
>     in the file; or

This implementation of inbound=outbound assumes that license information
will appear in contributed files, mostly likely in code header comments.

This is not the norm in npm package development, which prefers a
package-level `LICENSE` file and metadata in `package.json`'s `license`
property.

> (c) The contribution was provided directly to me by some other
>     person who certified (a), (b) or (c) and I have not modified
>     it.

Again, the AUTHORS Certificate lacks any analog to this language, due to

1. differences between kernel-style and pull-request-based development

2. a desire to require certification of original work

> (d) I understand and agree that this project and the contribution
>     are public and that a record of the contribution (including all
>     personal information I submit with it, including my sign-off) is
>     maintained indefinitely and may be redistributed consistent with
>     this project or the open source license(s) involved.

This language was added to DCO version 1.1 to address data privacy
regulation, especially, if Kernel Trap is to be believed, in Alan Cox'
native England.

Point of 5 of the AUTHORS Certificate is analogous, but does not
reference sign-off, a kernel-specific process. Point 5 also adds a
certification that the personal information provided for identification
does in fact identify the contributor, and that the contributor is not
adding information on behalf of anyone else.
