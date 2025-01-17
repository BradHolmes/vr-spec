Introduction
!!!!!!!!!!!!

Maximizing the personal, public, research, and clinical value of genomic information will require
that clinicians, researchers, and testing laboratories exchange genetic variation data reliably.
The Variation Representation Specification (VR-Spec) — written by a partnership among national
information resource providers, major public initiatives, and diagnostic testing laboratories — is
an open specification to standardize the exchange of variation data.

Here we document the primary contributions of this specification for variation representation:

* **Terminology and information model.** Definitions for biological terms may be abstract or
  intentionally ambiguous, often accurately reflecting scientific uncertainty or understanding at
  the time. Abstract and ambiguous terms are not readily translatable into a representation of
  knowledge. Therefore, the specification begins with precise computational definitions for
  biological concepts that are essential to representing sequence variation. The VR-Spec information
  model specifies how the computational definitions are to be represented in fields, semantics,
  objects, and object relationships.
* **Machine readable schema.** To be useful for information exchange, the information model should
  be realized in a schema definition language. The VR-Spec schema is currently implemented using JSON
  Schema, however it is intended to support translations to other schema systems (e.g. XML,
  OpenAPI, and GraphQL). The schema repository includes language-agnostic tests for ensuring schema
  compliance in downstream implementations.
* **Conventions that promote reliable data sharing.** The VR-Spec recommends conventions regarding
  the use of the schema and that facilitate data sharing.  For example, the VR-Spec recommends
  using fully justified allele normalization using an algorithm inspired by `NCBI's SPDI project
  <https://www.biorxiv.org/content/10.1101/537449v1>`__.
* **Globally unique computed identifiers.** This specification also recommends a specific algorithm
  for constructing distributed and globally-unique identifiers for molecular variation. Importantly, this
  algorithm enables data providers and consumers to computationally generate consistent, globally
  unique identifiers for variation without a central authority.
* **A reference implementation.** We provide a Python package (`vr-python
  <https://github.com/ga4gh/vr-python/>`__) that implements the above schema and algorithms, and
  supports translation of existing variant representation schemes into VR-Spec for use in genomic
  data sharing.

The machine readable schema definitions and example code are available online at the VR-Spec
repository (https://github.com/ga4gh/vr-spec).

