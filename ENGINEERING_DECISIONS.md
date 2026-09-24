# Engineering Decisions

## 1. Frontend/Backend Separation
The application keeps the frontend and backend responsibilities separate.

**Reason:** This makes the system easier to test, maintain, deploy, and extend.

## 2. REST API
The frontend communicates with the backend through REST endpoints.

**Reason:** REST provides a simple and familiar interface between the UI and server.

## 3. Server-Side Validation
Application data is validated on the server even when the frontend performs validation.

**Reason:** Frontend validation improves user experience, but server-side validation is required for trust and security.

## 4. Loading and Failure States
API-dependent screens show loading, success, empty/error, and retry states.

**Reason:** Users need clear feedback instead of a blank screen when network requests take time or fail.

## 5. Health Check
A dedicated `/health` endpoint reports whether the service is responding.

**Reason:** It provides a simple deployment and operational check.

## 6. Logging
The backend records useful request and error information.

**Reason:** Logs help identify failures and understand production behavior without exposing sensitive information.

## 7. Rate Limiting
Rate limiting is applied to appropriate API routes.

**Reason:** It reduces abuse and protects the API from excessive repeated requests.

## 8. Environment Variables
Environment-specific configuration and secrets are kept outside source code.

**Reason:** This prevents accidental exposure of credentials and makes deployment configuration safer.

## 9. Responsive Design
The UI is designed for mobile, tablet, and desktop screen sizes.

**Reason:** Internship applicants may use phones as well as computers.

## 10. Accessibility
Forms and interactive controls use labels, semantic HTML, keyboard support, focus states, and accessible error feedback.

**Reason:** The portal should be usable by people with different accessibility needs.

## 11. Testing
Automated tests and manual checks are used before submission.

**Reason:** Regression testing helps ensure that final polishing does not break functionality from earlier milestones.

## 12. Deployment
The application is deployed so the evaluator can test the real user journey.

**Reason:** A production-ready capstone should demonstrate behavior outside the local development environment.

## Architecture Summary

```text
User
  |
  v
Responsive Frontend
  |
  | REST/HTTP
  v
Backend API
  |
  +--> Validation
  +--> Rate Limiting
  +--> Logging
  +--> Database
  |
  v
Health / Monitoring
```

## Trade-offs
Document project-specific trade-offs here, for example:
- Why a particular database was selected.
- Why a particular hosting provider was selected.
- Why a particular validation library was selected.
- Any known limitations.

## Known Limitations
Add honest project-specific limitations here.
