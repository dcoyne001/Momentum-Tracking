# Template: Stripe Integration Task

## What I'm building
[e.g. "Subscription signup flow" / "Invoice payment link" / "Webhook handler"]

## Stripe objects involved
- [ ] Customer
- [ ] Subscription
- [ ] Payment Intent
- [ ] Invoice
- [ ] Webhook event: [event name e.g. `invoice.paid`]

## Supabase tables that need updating
[e.g. "Update `subscriptions` table when `customer.subscription.updated` fires"]

## Test mode / live mode
- [ ] Building in test mode (use Stripe test keys)
- [ ] Deploying to production

## Edge cases
- Payment failure / retry
- Trial expiry
- Cancellation mid-period

## Ask Claude to
- [ ] Write the Supabase Edge Function for the webhook
- [ ] Write the client-side checkout flow
- [ ] Handle error states
- [ ] Add idempotency key to prevent duplicate processing
