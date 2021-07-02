0.2.0 (unreleased)
------------------

-   Convert qrcode to template filter. In templates, change
    `{{ mfa_data.qrcode|safe }}` to `{% load mfa %} {{ mfa_data.url|qrcode }}`.
-   Fix form validation on missing code
-   Add german translation
-   use `never_cache` and `sensitive_post_parameters` decorators


0.1.0 (2021-06-29)
------------------

-   Trigger `user_login_failed` on failed second factor. This can be used to
    integrating with external rate limiting solutions such as django-axes.
-   Fix: include JS files in python package
-   Render qrcode server-side
-   Convenience: redirect to TOTP auth if no FIDO2 key exists
-   Add optional `MFAEnforceMiddleware`
-   Tweak admin UI
-   Tweak example templates


0.0.0 (2021-06-21)
------------------

initial release