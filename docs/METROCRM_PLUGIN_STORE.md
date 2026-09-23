# MetroCRM Plugin Store Foundation

This branch contains the initial reusable plugin catalog for the Om Krishna Group Plugin Store.

## Purpose

MetroCRM capabilities are represented as assignable plugins so a company can be provisioned with only the CRM modules it needs.

## Plugin groups

- Core CRM: Leads, Customers, Requirements, Assignment, Follow-ups, Calls, Site Visits
- Property: Developers, Projects, Towers, Units, Nearby Locations, Property Data, Media
- Communication: WhatsApp CRM, WhatsApp Property Import, Email, Missed Call
- AI: AI Caller, AI Call Logs
- Administration: Users, RBAC, Audit, Export Control
- Analytics: Dashboard, Reports, Lead Sources
- Integrations: Integration Manager, Website Lead Capture
- System: Backup & Restore

## Security rules

1. Plugin assignment controls feature availability; it is not a substitute for authorization.
2. Every plugin must enforce the existing authenticated-user role/permission checks.
3. Company data isolation must be enforced server-side.
4. Disabling a plugin must not delete its data.
5. System-only functions such as backup/restore must never become tenant-admin controls.
6. Secrets/API credentials must not be stored in this catalog.

## Next implementation step

Integrate this catalog with the existing Om Krishna Group admin/plugin UI, then add company-level plugin assignment and activation state. Do not change MetroCRM production code until the plugin contract is reviewed.
