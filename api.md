# JackAI Platform OS Hub API (public subset) Python API

<!-- omniwrap-api-reference eyJjb250cmFjdF9maW5nZXJwcmludCI6ImM3Y2E1ZTVlYmI0YzA5MjkxMGVjNzJiMzcxZTE4ODMwMzM1OGM1ZTM0ZDI5MDhjMGE4OGY3ODJhMjQxMTYyY2YiLCJvcGVyYXRpb25fY291bnQiOjgsInJlbmRlcmVyIjoicHl0aG9uIiwidmVyc2lvbiI6IjEuNS4wIn0 -->

This generated index is tied to Semantic IR `1.14.0` and contract fingerprint `c7ca5e5ebb4c092910ec72b371e188303358c5e34d2908c0a88f782a241162cf`. Every operation below is rendered from the same semantic contract and artifact-attested public member allocation as the SDK.

SDK maturity: **experimental**  
Artifact evidence: [`omniwrap-artifact.json`](omniwrap-artifact.json) binds this file by SHA-256 and is revalidated by the package gate.

## Client hooks and tracing

`Client(hooks=Hooks(...))` registers four callbacks. Every attempt starts with `before_request` and ends with exactly one of `on_retry` (another attempt follows), `after_response` (the success the call returns) or `on_error` (the failure the call reports). Each receives the operation id, the HTTP method, the URL, the request headers, the attempt number (from 1), the time elapsed since the call started and, once the server answered, the HTTP status. No context carries a credential: `Authorization`, `Proxy-Authorization`, `Cookie`, every API-key header and API-key query parameter, and any configured credential value read `[redacted]`. Every context is a frozen `HookContext`: no hook can change the request.

`Client(tracer=...)` opens one span per call through the tracer interface this SDK defines, named after the operation id, with `http.request.method`, `http.response.status_code` and `http.request.resend_count`. It needs no tracing library; README.md maps it onto the OpenTelemetry API.

## Resource `health`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJoZWFsdGguZ2V0IiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoiZ2V0SGVhbHRoIiwicGF0aCI6Ii9oZWFsdGgiLCJyZXNvdXJjZSI6ImhlYWx0aCIsInNlY3Rpb25fc2hhMjU2IjoiZTE4ZjE5MGYzNDRkM2UyY2I5NGQyZWM5NzJkZTVkMGIxMDk4MWQ1OTUxNDUzNTA2MGMzMGYwMWJmYmQ1NDY1ZSIsInNpZ25hdHVyZV9zaGEyNTYiOiIxOWRiZmQ0MTM1N2I1ZWZlNzVhNjU5YzA5ZjNiNWU5ZjY5YWY0YzUwNDViNTJiZGM5NmRjNzNlN2QzNjkzNWM0In0 -->
### `client.health.get`

Operation ID: `getHealth`  
Route: `GET` `/health`  
Equivalent member: `client.get_health`  

#### Signature

```python
client.health.get(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Hub liveness status | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.health.get()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRIZWFsdGgifQ -->

## Resource `kernel`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJrZXJuZWwuZmFpbF91c2FnZV9xdW90YSIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJmYWlsVXNhZ2VRdW90YSIsInBhdGgiOiIvdjEva2VybmVsL3VzYWdlL2ZhaWwiLCJyZXNvdXJjZSI6Imtlcm5lbCIsInNlY3Rpb25fc2hhMjU2IjoiZThkNzkzNjFjNzMzYjY2MzZmYmRjMzE2OGM3MGVlMGNkNmY0ZWZmNTY1Y2U4MGU1Zjg0ZGU0NmM5NTVhNDg0YiIsInNpZ25hdHVyZV9zaGEyNTYiOiJmYzY1MWYwMWY0MjkxYjNkNDU3ODY3ZTcyMmY0NjJjNDc4MWYxODVlODRiZGM3NTczMWM1OTMzYzFjYTU2NzliIn0 -->
### `client.kernel.fail_usage_quota`

Operation ID: `failUsageQuota`  
Route: `POST` `/v1/kernel/usage/fail`  
Equivalent member: `client.fail_usage_quota`  

#### Signature

```python
client.kernel.fail_usage_quota(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Reservation released | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.kernel.fail_usage_quota()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJmYWlsVXNhZ2VRdW90YSJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJrZXJuZWwuZmluYWxpemVfdXNhZ2VfcXVvdGEiLCJtZXRob2QiOiJQT1NUIiwib3BlcmF0aW9uX2lkIjoiZmluYWxpemVVc2FnZVF1b3RhIiwicGF0aCI6Ii92MS9rZXJuZWwvdXNhZ2UvZmluYWxpemUiLCJyZXNvdXJjZSI6Imtlcm5lbCIsInNlY3Rpb25fc2hhMjU2IjoiOGJlYTUyYmU2N2UxZDEwMWIxMDc3NDAyZTQwZmY5NThlZThlYjExMzE4MTcwYzg4MDQ0MTExZWQ4MGYwYjdlZiIsInNpZ25hdHVyZV9zaGEyNTYiOiI4NmE2ZDM4NzBlNTVjNzA3NGNlZGRkYjJhNTg1N2YxZDcwNzA1ZjlmNTY3M2JhYjIyYTFlMDY1ZDM0Y2IwZGIyIn0 -->
### `client.kernel.finalize_usage_quota`

Operation ID: `finalizeUsageQuota`  
Route: `POST` `/v1/kernel/usage/finalize`  
Equivalent member: `client.finalize_usage_quota`  

#### Signature

```python
client.kernel.finalize_usage_quota(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Reservation finalized | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.kernel.finalize_usage_quota()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJmaW5hbGl6ZVVzYWdlUXVvdGEifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJrZXJuZWwucmVzZXJ2ZV91c2FnZV9xdW90YSIsIm1ldGhvZCI6IlBPU1QiLCJvcGVyYXRpb25faWQiOiJyZXNlcnZlVXNhZ2VRdW90YSIsInBhdGgiOiIvdjEva2VybmVsL3VzYWdlL3Jlc2VydmUiLCJyZXNvdXJjZSI6Imtlcm5lbCIsInNlY3Rpb25fc2hhMjU2IjoiMTcyNTlhNDBjNTFiMTE3ZjZhNmVlNjE5OTY4NDg3YjUwMGU3NDUzMGFjOWZmYzBiYjVmMGZkMWQ0NDUxODQxNyIsInNpZ25hdHVyZV9zaGEyNTYiOiIxMjg2ZTJhYjk3ZmZkNzg1Y2FkNWM5MzY1ZTkzYzFiNWFiMGEwMDMxNDFjNDE5NmIyYTdkNjM1MzYzMTNhMjQ5In0 -->
### `client.kernel.reserve_usage_quota`

Operation ID: `reserveUsageQuota`  
Route: `POST` `/v1/kernel/usage/reserve`  
Equivalent member: `client.reserve_usage_quota`  

#### Signature

```python
client.kernel.reserve_usage_quota(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Reservation lease created | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.kernel.reserve_usage_quota()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJyZXNlcnZlVXNhZ2VRdW90YSJ9 -->

## Resource `user`

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ1c2VyLmdldF9jdXJyZW50IiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoiZ2V0Q3VycmVudFVzZXIiLCJwYXRoIjoiL3VzZXIvbWUiLCJyZXNvdXJjZSI6InVzZXIiLCJzZWN0aW9uX3NoYTI1NiI6IjU2MDgyY2EyN2U5ODNkMTY5NTRiOGMwNzliZDRkMmE3NjRlNDhiZGMyOWNlZmZkNzQ1YmM5OGFmYzNiMWJjZjIiLCJzaWduYXR1cmVfc2hhMjU2IjoiZjliNzgzMGI4ZjI3MTIxZGQ1ZTEzMDRlMmEyZGJhNjU2MWVjYWRkNDg0ZjJiYzUwNGI3ZjAxMDgzYWMwODZmMCJ9 -->
### `client.user.get_current`

Operation ID: `getCurrentUser`  
Route: `GET` `/user/me`  
Equivalent member: `client.get_current_user`  

#### Signature

```python
client.user.get_current(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Current user context | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.user.get_current()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRDdXJyZW50VXNlciJ9 -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ1c2VyLmdldF9zaWdudXBfcG9saWN5IiwibWV0aG9kIjoiR0VUIiwib3BlcmF0aW9uX2lkIjoiZ2V0U2lnbnVwUG9saWN5IiwicGF0aCI6Ii91c2VyL2F1dGgvc2lnbnVwLXBvbGljeSIsInJlc291cmNlIjoidXNlciIsInNlY3Rpb25fc2hhMjU2IjoiYjFlYWY1MTMyZTg3YzU2YmRkYzZjYTEwM2Q5OGMzNTI0YWU4ZGRhNzEyNDg5NzMzYjBhZDVmNTY2ZWZkOTMxMSIsInNpZ25hdHVyZV9zaGEyNTYiOiI2ODljZWNkNDYzNGYwZGNiODdiZDVjMjczNjIxMTJjYzA2MzBkOWRhMTYyOTNkNzRkZjZjMzc1ZmIxMDU1ZmFkIn0 -->
### `client.user.get_signup_policy`

Operation ID: `getSignupPolicy`  
Route: `GET` `/user/auth/signup-policy`  
Equivalent member: `client.get_signup_policy`  

#### Signature

```python
client.user.get_signup_policy(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Current signup policy | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.user.get_signup_policy()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJnZXRTaWdudXBQb2xpY3kifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ1c2VyLmxvZ2luIiwibWV0aG9kIjoiUE9TVCIsIm9wZXJhdGlvbl9pZCI6ImxvZ2luVXNlciIsInBhdGgiOiIvdXNlci9hdXRoL2xvZ2luIiwicmVzb3VyY2UiOiJ1c2VyIiwic2VjdGlvbl9zaGEyNTYiOiJlZWQxOTUyYWU3MzM1MDVmZTQ0MWNiNWU4ZmZhZjM1NjA0OWU3MjhiYzUwM2MyOTFjMzdmNzdhMDJmZjE4NGRmIiwic2lnbmF0dXJlX3NoYTI1NiI6ImU4MTgxNjRmYmFkYjJjZWMyMGJmNmM3ZGU0YzcxYmM2ZmY1YjRiOWMyYTNmOWNiZjU4OWQwNjdjYzIxNzg1ZTkifQ -->
### `client.user.login`

Operation ID: `loginUser`  
Route: `POST` `/user/auth/login`  
Equivalent member: `client.login_user`  

#### Signature

```python
client.user.login(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `200` | Authenticated session or MFA challenge | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.user.login()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJsb2dpblVzZXIifQ -->

<!-- omniwrap-api-operation eyJleGFtcGxlX3JlYXNvbiI6bnVsbCwiZXhhbXBsZV9zdGF0dXMiOiJnZW5lcmF0ZWQiLCJtZW1iZXIiOiJ1c2VyLnN1Ym1pdF93YWl0bGlzdF9yZXF1ZXN0IiwibWV0aG9kIjoiUE9TVCIsIm9wZXJhdGlvbl9pZCI6InN1Ym1pdFdhaXRsaXN0UmVxdWVzdCIsInBhdGgiOiIvdXNlci9hdXRoL3dhaXRsaXN0IiwicmVzb3VyY2UiOiJ1c2VyIiwic2VjdGlvbl9zaGEyNTYiOiI4NGNiMjliOGQ0NzJmNTYzZGIxNTk3NGFiMzRmMjgxMjBkNWU5Y2M5NDBjZDNlNTZjZTk2NDYwNjhmNjBhNzg3Iiwic2lnbmF0dXJlX3NoYTI1NiI6ImJkYjY2ZmFmMjBlZThhM2E2NzQ5MWI4NmNmMDMyYjVjZTlhNTllZTJjYmE0N2QzODJiZjAxMzI4Y2FiZTA3YTUifQ -->
### `client.user.submit_waitlist_request`

Operation ID: `submitWaitlistRequest`  
Route: `POST` `/user/auth/waitlist`  
Equivalent member: `client.submit_waitlist_request`  

#### Signature

```python
client.user.submit_waitlist_request(*, headers: Optional[Mapping[str, str]] = None, query: Optional[Mapping[str, Any]] = None, cookies: Optional[Mapping[str, str]] = None, timeout: Optional[float] = None, max_retries: Optional[int] = None, max_response_bytes: Optional[int] = None, idempotency_key: Optional[str] = None) -> None
```

#### Parameters

| Name | In | Required | Contract type | Description |
| --- | --- | --- | --- | --- |
| _none_ | | | | |

#### Responses

| Status | Description | Content |
| --- | --- | --- |
| `202` | Waitlist request recorded with an opaque WL- reference | none |

#### Canonical required-input example

```json
{
  "parameters": []
}
```

#### SDK call example

Example status: `generated`  
```python
result = client.user.submit_waitlist_request()
```

<!-- omniwrap-api-operation-end eyJvcGVyYXRpb25faWQiOiJzdWJtaXRXYWl0bGlzdFJlcXVlc3QifQ -->

