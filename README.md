# YAML-based Org Charts

Over my career, one thing has been a recurring drag on not just effective
security solutions, but just general engineering work, has been the lack of
an easy to access, process, and query org chart. Inspired by the work many
_other people_ did at my previous employer around an internal system (called
Roster), I've turned this into something even simpler: a YAML file.

I have done this as a [JSON Schema](https://json-schema.org) to make it
easier to validate. At the minimum, you only need a `name` and `active`
status. Everything else can be done incrementally.
