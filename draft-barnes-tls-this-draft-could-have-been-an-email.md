---
title: "Stop Doing Cryptographic Algorithm Drafts when Email to IANA is All You Need"
abbrev: "No More Crypto"
category: info

docname: draft-barnes-tls-this-draft-could-have-been-an-email-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: "Security"
workgroup: "Transport Layer Security"
keyword:
 - next generation
 - unicorn
 - sparkling distributed ledger
venue:
  group: "Transport Layer Security"
  type: "Working Group"
  mail: "tls@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/tls/"
  github: "bifurcation/no-more-crypto"
  latest: "https://bifurcation.github.io/no-more-crypto/draft-barnes-tls-this-draft-could-have-been-an-email.html"

author:
 -
    fullname: Richard Barnes
    organization: Cisco
    email: rlb@ipv.sx

normative:

informative:

...

--- abstract

People keep pitching drafts to the TLS Working Group where the only thing the
draft does is register a code point for a cryptographic algorithm.  Stop doing
that.  It's unnecessary.  Write an email to IANA instead.

--- middle

# Introduction

There used to be a grand tradition of debating the merits of cryptographic
algorithms in the TLS working group.  Over time, folks realized that this was
not a productive use of the WG's time.  The typical TLS WG participant is not a
cryptographer, and the cryptographic choices of TLS users are typically dictated
by other factors than the opinion of the TLS WG.

As a result, {{!RFC8447}} loosened the registration policy on the TLS registries
to Specification Required, with a very limited carve-outs related to the
"Recommended" column.  As a result, anyone can register a code point for a
cryptographic algorithm with a stable public specification, without having to
convince the TLS WG of anything.  Registration is as simple as one email to
<iana@iana.org>.

This document proposes that the TLS WG adopt a restrictive policy that if the
only thing a document does could be done without the WG, that document will not
be adopted.

# Conventions and Definitions

{::boilerplate bcp14-tagged}

# When Are Crypto Documents OK?

The registry policies in {{RFC8447}} define a few specific things that require
working group action.

* Initial registration with Recommended=Y
* Changing the value of the Recommended column to "Y" or "D" from something else
* Changing the value of the Recommended column from "Y" or "D" to something else

Unless a document does one of these things it MUST NOT be adopted by the WG.
Even if there are additional technical details to be specified, the proponents
can publish their own specification; even an individual -00 Internet-draft meets
IANA's criteria for a stable, public specification.

For example:

* {{?I-D.ietf-tls-mlkem}} and {{?I-D.ietf-tls-mldsa}} define technical details,
  but do not request Recommended=Y.  The authors could have simply published
  these details on their own (e.g., in an individual Internet-draft) and
  requested code points.

* {{?I-D.reddy-tls-slhdsa}} simply registers SLH-DSA code points, pointing to
  the existing FIPS documents for all technical details.  Nonetheless, it has
  consumed a significant amount of WG time, including multiple challenges and
  appeals.

Authors that just want to register a code point should skip the working group
and go directly to IANA.  It's easier, it's faster, and it won't waste a bunch
of other folks' time in the working group.

# Security Considerations

The policy proposed in this document has no impact on security.  The registry
policies already allow any algorithm with a specification to be registered.
Let's just not spend the WG's time debating things that the WG doesn't need to
opine on.

# IANA Considerations

This document has no IANA actions.  Ironically.

--- back
