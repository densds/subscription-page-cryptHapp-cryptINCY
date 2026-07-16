## Remnawave Subscription Page

### INCY encrypted subscription links

This fork adds support for INCY encrypted deep links (`incy://crypt1/...`), similar to
the existing `HAPP_CRYPT4_LINK` placeholder for Happ.

**Setup:**
1. Install the dependency in `backend`: `npm install @incy/link-encoder`
2. In your app-config JSON (Subscription Page settings), use the placeholder
   `{{INCY_CRYPT1_LINK}}` as the `link` value for an INCY button.

The backend validates that the subscription actually exists before encrypting the
link (via the same `getSubscriptionInfo` call used to serve the subscription page),
and builds the URL from the request's own host — the client never supplies an
arbitrary URL to encrypt.

Learn more about Remnawave [here](https://remna.st/).

# Contributors

Check [open issues](https://github.com/remnawave/subscription-page/issues) to help the progress of this project.

<p align="center">
Thanks to the all contributors who have helped improve Remnawave:
</p>
<p align="center">
<a href="https://github.com/remnawave/subscription-page/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=remnawave/subscription-page" />
</a>
</p>
