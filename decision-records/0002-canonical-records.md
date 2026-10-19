# 0002: Canonical records and generated navigation

Date: 2026-10-19  
Status: Proposed in restructuring pull request  
Independent reviewer: Pending

## Problem

The repository grew by adding overlapping category pages, industry tables, profiles and batch appendices. Counts and verification statements became stale. Some entries existed only in YAML while others had profiles under ownership or category folders.

## Decision

Give every catalogue ID one canonical narrative record under catalogue/records and keep structured metadata in catalogue/index.yaml. Make category and ownership views generated navigation, not second descriptions. Keep industry context separate from sources and evidence. Store cases and exceptions together under evidence with explicit finding types. Preserve uncatalogued sources in a deduplicated backlog and historical proposals in the archive.

## Consequences

Paths change and external deep links must be updated. IDs, sources and substantive evidence remain available. Source-check status is not upgraded by the restructure. Local checks prevent duplicate IDs, missing profiles, broken links and stale generated inventories.

## Alternatives

Keeping old browse pages would retain competing descriptions. Adding redirect files everywhere would preserve duplicate directory trees. A single catalogue with linked views gives readers a simpler, maintainable route.

## Reconsideration

If the hub adopts a documentation site, generate navigation from the same metadata instead of introducing another catalogue.
