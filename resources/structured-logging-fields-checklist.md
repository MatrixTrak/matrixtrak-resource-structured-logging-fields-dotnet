# Structured logging fields checklist (.NET)

Use this during incidents to confirm you can explain what failed, why it failed, and where the time went.

## Required request fields

- correlation_id
- request_id
- route
- method
- status_code
- duration_ms
- result_class (success, transient_failure, permanent_failure)

## Required dependency fields

- dependency_name
- dependency_type (http, sql, cache, queue)
- dependency_duration_ms
- dependency_status
- timeout_ms

## Required retry and timeout fields

- retry_attempt
- retry_max
- retry_wait_ms
- timeout_result (none, canceled, timed_out)

## Required context fields

- service
- instance
- environment
- version

## Checks

- Field names are identical across services.
- Duration fields are integers and measured in milliseconds.
- High cardinality fields are not promoted to top level.
- Trace id and span id are logged on errors and slow requests.
