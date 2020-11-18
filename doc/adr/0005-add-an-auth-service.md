# 5. Add an Auth service

Date: 2020-11-08

## Status

Accepted

## Context

Multiple services will need user information, and know who can access what. Later on we might also need
to add multiple registration features such as confirmation emails, 2FA, and so on.

## Decision

Add a dedicated service to handling authentication and authorization.

## Consequences

Adding new security policies and features will be localized to this service.
