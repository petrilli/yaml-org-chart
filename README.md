# YAML-based Org Charts

Over my career, one thing has been a recurring drag on not just effective
security solutions, but just general engineering work, has been the lack of
an easy to access, process, and query org chart. Inspired by the work many
_other people_ did at my previous employer around an internal system (called
Roster), I've turned this into something even simpler: a YAML file.

I have done this as a [JSON Schema](https://json-schema.org) to make it
easier to validate. At the minimum, you only need a `name` and `active`
status. Everything else can be done incrementally.

There are a few areas that need to be considered if you adopt this:

1. Do you use an `id` for organizations? The advantage is that you have a
   stable identifier for the organization. The disadvantage is having to
   create them (not hard, but...). Alternatively, if you can be sure the
   top-level property identifier is stable, then that is a reasonable
   reference.
2. A taxonomy for `contact-method`. For this to be useful, you will need to
   decide what contact methods are important and what identifiers would be
   used. I would recommend you define this early and ensure that you
   validate it.