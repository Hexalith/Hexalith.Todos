# Claude Instructions

## Repository Boundaries

- Treat this repository root as the workspace boundary.
- Reference projects only when they are in this repository or in child folders of this repository.
- Do not reference projects from parent folders or sibling folders of this repository.

## Module Ownership

- This repository is a domain module for Todos.
- Keep Todo domain-centric code in this repository.
- Put common or technical code in the appropriate submodule instead of this repository.
- Put persistence and event store code in `Hexalith.EventStore`.
- Put generic shared/common code in `Hexalith.Commons`.
- Put tenant management code in `Hexalith.Tenants`.
- Put party management code in `Hexalith.Parties`.

## Running Servers

- Use .NET Aspire to manage and run servers for this repository.
- Prefer the Aspire AppHost and Aspire dashboard for starting, stopping, inspecting, and diagnosing application resources.
- Do not start individual server projects directly when an Aspire AppHost is available.

## Submodules

- Initialize submodules only at the root of this repository.
- Do not initialize, update, or recurse into submodules nested inside submodules.
- Avoid recursive submodule commands such as `git submodule update --init --recursive`.
