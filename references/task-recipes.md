# Agent task recipes

Corpus SHA-256: `6427b015c23dd2a3b1acc22ebf3e94d8a4db9b807787ca9ceb800ea6cfcbc3f0`

These recipes are retrieval and planning evidence. They never authorize API execution.

## `authentication-failusagequota-bearerauth` — authentication

How is bearerAuth authentication applied to failUsageQuota? Cite exactly: operation:failUsageQuota, auth:bearerAuth

Intent: Recover the exact authentication scheme, location or flow, and required scopes.

Expected evidence:

- operation: `failUsageQuota`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/failUsageQuota`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-failusagequota` — discovery

Find the exact operation failUsageQuota (POST /v1/kernel/usage/fail) for Release the reserved quota of an execution that failed or was cancelled. Cite exactly: operation:failUsageQuota, auth:bearerAuth

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `failUsageQuota`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/failUsageQuota`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-finalizeusagequota` — discovery

Find the exact operation finalizeUsageQuota (POST /v1/kernel/usage/finalize) for Phase 2 of atomic 2-phase quota metering: commit actual consumed credits. Cite exactly: operation:finalizeUsageQuota, auth:bearerAuth

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `finalizeUsageQuota`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/finalizeUsageQuota`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-getcurrentuser` — discovery

Find the exact operation getCurrentUser (GET /user/me) for Retrieve current user profile, organizations, and active security posture. Cite exactly: operation:getCurrentUser, auth:bearerAuth

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `getCurrentUser`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/getCurrentUser`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-gethealth` — discovery

Find the exact operation getHealth (GET /health) for Check that the Hub API process is up. Cite exactly: operation:getHealth, auth:bearerAuth

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `getHealth`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/getHealth`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-getsignuppolicy` — discovery

Find the exact operation getSignupPolicy (GET /user/auth/signup-policy) for Inspect current V1 user registration policy (waitlist vs open self-service). Cite exactly: operation:getSignupPolicy, auth:bearerAuth

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `getSignupPolicy`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/getSignupPolicy`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-loginuser` — discovery

Find the exact operation loginUser (POST /user/auth/login) for Authenticate user credentials and issue host-only session or step-up MFA challenge. Cite exactly: operation:loginUser, auth:bearerAuth

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `loginUser`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/loginUser`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-reserveusagequota` — discovery

Find the exact operation reserveUsageQuota (POST /v1/kernel/usage/reserve) for Phase 1 of atomic 2-phase quota metering: reserve credits before task execution. Cite exactly: operation:reserveUsageQuota, auth:bearerAuth

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `reserveUsageQuota`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/reserveUsageQuota`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `discovery-submitwaitlistrequest` — discovery

Find the exact operation submitWaitlistRequest (POST /user/auth/waitlist) for Record a prospective customer access request while V1 public signup is gated. Cite exactly: operation:submitWaitlistRequest, auth:bearerAuth

Intent: Identify the operation without inventing a route or method.

Expected evidence:

- operation: `submitWaitlistRequest`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/submitWaitlistRequest`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-failusagequota` — integration

Plan a correct SDK integration for failUsageQuota (POST /v1/kernel/usage/fail). Cite exactly: operation:failUsageQuota, auth:bearerAuth

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `failUsageQuota`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/failUsageQuota`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-finalizeusagequota` — integration

Plan a correct SDK integration for finalizeUsageQuota (POST /v1/kernel/usage/finalize). Cite exactly: operation:finalizeUsageQuota, auth:bearerAuth

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `finalizeUsageQuota`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/finalizeUsageQuota`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-getcurrentuser` — integration

Plan a correct SDK integration for getCurrentUser (GET /user/me). Cite exactly: operation:getCurrentUser, auth:bearerAuth

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `getCurrentUser`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/getCurrentUser`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-gethealth` — integration

Plan a correct SDK integration for getHealth (GET /health). Cite exactly: operation:getHealth, auth:bearerAuth

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `getHealth`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/getHealth`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-getsignuppolicy` — integration

Plan a correct SDK integration for getSignupPolicy (GET /user/auth/signup-policy). Cite exactly: operation:getSignupPolicy, auth:bearerAuth

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `getSignupPolicy`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/getSignupPolicy`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-loginuser` — integration

Plan a correct SDK integration for loginUser (POST /user/auth/login). Cite exactly: operation:loginUser, auth:bearerAuth

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `loginUser`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/loginUser`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-reserveusagequota` — integration

Plan a correct SDK integration for reserveUsageQuota (POST /v1/kernel/usage/reserve). Cite exactly: operation:reserveUsageQuota, auth:bearerAuth

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `reserveUsageQuota`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/reserveUsageQuota`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.

## `integration-submitwaitlistrequest` — integration

Plan a correct SDK integration for submitWaitlistRequest (POST /user/auth/waitlist). Cite exactly: operation:submitWaitlistRequest, auth:bearerAuth

Intent: Recover exact wire parameters, request media, responses, and safety traits.

Expected evidence:

- operation: `submitWaitlistRequest`
- authentication: `bearerAuth`
- criterion: return the expected entity identifiers
- criterion: cite only resolvable OmniWrap resources
- criterion: stay within the declared result, context, and tool-call budgets
- criterion: perform none of the forbidden actions

Citations:

- `omniwrap://semantic/auth/bearerAuth`
- `omniwrap://semantic/operation/submitWaitlistRequest`

Budgets: at most 5 results, 8192 context bytes, and 3 tool calls.
