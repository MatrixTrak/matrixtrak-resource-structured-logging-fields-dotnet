# Structured logging fields checklist (.NET)

This kit provides a minimal schema and starter configuration for incident ready logs in .NET services.

## Files

- structured-logging-fields-checklist.md
- serilog-json-starter.json
- example-error-log.json

## How to use

1. Add the schema fields to your request and dependency logs.
2. Keep field names and types consistent across services.
3. Log trace id and span id on errors and slow requests.

## Notes

- Do not promote high cardinality payloads to top level fields.
- Keep the schema small and stable so queries remain fast.
