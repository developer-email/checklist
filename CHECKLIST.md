# Pre-production checklist

## Keys and security

- [ ] API key stored in server env only (not in the browser)
- [ ] Prefer send-scoped / domain-locked keys for apps when available
- [ ] `.env` files gitignored; only `.env.example` committed
- [ ] No keys in screenshots, issues, or chat logs

## Domain and DNS

- [ ] Sending domain chosen and documented
- [ ] SPF / DKIM published; DMARC planned
- [ ] Production custom `from` only after verification succeeds
- [ ] Understood sandbox vs production lock (if provider has one)

## Sending paths

- [ ] Password reset / magic link / receipt flows identified
- [ ] HTML rendered by the app (or agent)—no need for a template studio unless you want one
- [ ] Failure handling for 4xx/5xx and provider error codes
- [ ] Idempotency / dedupe considered for webhooks and retries

## Observability

- [ ] Can find a send in logs by message id
- [ ] Bounce / complaint handling path exists (webhook or dashboard)
- [ ] Alerts for sudden failure spikes (even a simple Slack webhook)

## Ops

- [ ] Who rotates keys?
- [ ] Who owns DNS changes?
- [ ] Free-tier limits known (emails/mo, log retention, webhooks)

## Optional but valuable

- [ ] Staging uses sandbox/test send
- [ ] Coding agents use MCP/skills without pasting keys into chat
