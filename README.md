## Surakiart Yasaka

QA engineer. I build the tooling around testing — the things that decide who can
run what, where the result goes, and how you reproduce a failure later.

**[testbydesign.dev](https://testbydesign.dev)** — all of it in one place, with
the request paths drawn out.

These are rebuilds of work I did at a company, published so the approach can be
read. The architecture, the decisions and the operational habits travelled; the
employer's code, business domain and branding did not.

---

**[playwright-run-dashboard](https://github.com/surakiartysk/playwright-run-dashboard)** · [live](https://runs.testbydesign.dev)

Self-service test running: pick a slice, press Run, get a link to the report.
The interesting part is not the Run button — it is who may run what against
which branch, and who may then see the result. Four roles, four dashboards, and
a `demo` role that can never trigger a real run, which is what makes its
password safe to publish.

React · Cloudflare Workers · D1 · R2

**[playwright-api-automation-patterns](https://github.com/surakiartysk/playwright-api-automation-patterns)**

The same API suite built twice against one contract — one functional, one
class-first — so the approaches can be read side by side. 97 tests each,
verified by mutating the mock and checking both suites fail identically. The
finding worth keeping: removing the status-code check from the shared assertion
helper left every test passing in both packages. That is a property of
centralising assertions, not of either style.

Playwright · TypeScript · Allure

**[paygate-sandbox](https://github.com/surakiartysk/paygate-sandbox)** · [live](https://paygate-sandbox.vercel.app)

A sandbox that emulates the 2C2P and Omise payment APIs, so an integration can
be tested against the responses a real staging environment will not produce on
demand: declines with a specific code, duplicate webhooks, out-of-order
callbacks, timeouts. Your backend is unchanged; a second API drives the outcome.

Node · Vercel

---

[LinkedIn](https://www.linkedin.com/in/surakiartysk/)
