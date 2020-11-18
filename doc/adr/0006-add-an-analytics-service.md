# 6. Add an analytics service

Date: 2020-11-08

## Status

Accepted

## Context

We need to provide information about who's visting a user's links in a understandable format
like a dashboard on a website.
This system is just built on top of the redirect service, and is a separate concern.

## Decision

We will havea dedicated service to previewing analytics information on visitors.

## Consequences

Adding more analytics features is localized to this service. But if the changes require
gathering other types of data, then it will also affect the redirect service

The analytics service will be decoupled from the main system. While it will not be able
to fetch the latest data, it will still function on its own.
