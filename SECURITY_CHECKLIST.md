# Security Checklist

## Application Security

- [ ] Server-side validation is implemented.
- [ ] Frontend validation does not replace backend validation.
- [ ] Required fields are validated.
- [ ] Email/input formats are validated.
- [ ] Input length limits are enforced.
- [ ] Invalid IDs/requests are rejected.
- [ ] Database queries use safe parameterization.
- [ ] Sensitive values are stored in environment variables.
- [ ] `.env` files containing secrets are excluded from Git.
- [ ] `.env.example` contains only placeholder values.
- [ ] CORS allows only required origins in production.
- [ ] API rate limiting is enabled where appropriate.
- [ ] Error responses do not expose stack traces.
- [ ] Database/internal errors are not sent directly to clients.
- [ ] Security-sensitive logs do not contain passwords, tokens, or unnecessary personal data.
- [ ] Dependencies are checked for known vulnerabilities.
- [ ] HTTPS is used by the deployed application where supported.

## Form Security

- [ ] Form fields have server-side validation.
- [ ] Unexpected fields are handled safely.
- [ ] Oversized input is rejected.
- [ ] User-facing error messages are safe and useful.
- [ ] Duplicate/abusive submissions are considered.

## Deployment Security

- [ ] Production secrets are configured through the hosting provider.
- [ ] Debug mode is disabled in production.
- [ ] Source control contains no API keys or passwords.
- [ ] CORS configuration is reviewed before deployment.
- [ ] Production health endpoint works.

## Final Verification

Reviewer:
`ADD_NAME`

Date:
`ADD_DATE`

Result:
`NOT VERIFIED`

Notes:
`ADD_NOTES`
