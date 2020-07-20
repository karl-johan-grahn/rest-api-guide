# REST API guide

| Meta | Content |
| ------------ | ------------ |
| Author | Karl-Johan Grahn |
| Editorially approved | 20 July 2020 |
| Last updated | 20 July 2020 |

# Table of contents

- [1. Introduction](#1-introduction)
- [2. Principles](#2-principles)
- [3. Requirements](#3-requirements)
  - [Resources](#resources)
  - [Versioning](#versioning)
  - [Long running operations](#long-running-operations)
  - [Compatibility](#compatibility)
- [4. Governance](#4-governance)
- [5. Support](#5-support)

# 1. Introduction

REpresentational State Transfer (REST) is a common API architectural style. It is not a standard, but it is without doubt the [most common API style in use](https://www.programmableweb.com/news/which-api-types-and-architectural-styles-are-most-used/research/2017/11/26).

[Roy Fielding's PhD thesis](https://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm) is the canonical source for the style.

This guide describes how REST is meant to be used.

# 2. Principles
- What is an API?
- What is REST?
- What is a REST API?
- Why is it important?

# 3. Requirements
*Focus on examples*

The API must follow these requirements:

## Resources
A fundamental concept in a REST API is resources.
- Avoid verbs
Valid example: `GET /accounts/{ID}`
Invalid example: `GET /return-all-accounts/{ID}`
- Use sub-paths
- ...

## Versioning
## Long running operations
## Compatibility

# 4. Governance
The `API governance service` will validate the API endpoints for each service. When the service goes through the `build pipeline`, API validation is a build step before being able to deploy to the `stage environment`.

The `API gateway` will override the requests and provide a `governance` field as part of response:
```json
{
  "governance": "approved",
  "...": ...
}
```
# 5. Support
For support, please contact @karl-johan-grahn
