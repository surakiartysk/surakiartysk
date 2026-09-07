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
a `demo` role that can never trigger a real run — which is why it needs no
password at all, just a button.

React · Cloudflare Workers · D1 · R2

**[playwright-api-automation-patterns](https://github.com/surakiartysk/playwright-api-automation-patterns)**

The same API suite built twice against one contract — one functional, one
class-first — so the approaches can be read side by side. 97 tests each,
verified by mutating the mock and checking both suites fail identically. The
finding worth keeping: removing the status-code check from the shared assertion
helper left every test passing in both packages. That is a property of
centralising assertions, not of either style.

Playwright · TypeScript · Allure

**[playwright-ui-automation-patterns](https://github.com/surakiartysk/playwright-ui-automation-patterns)**

The same question asked of browser tests. "Use page objects" is where most UI
advice stops and it settles nothing — it says nothing about where the knowledge
of the page should live. Two answers built side by side, held to the same ten
journeys by a check that fails when either is missing one. The finding worth
keeping: neither structure made a wrong test easier to write. Both would assert
on a cart badge while the cart behind it was empty, and what caught that was
mutation testing, not the way the suite was organised.

Playwright · TypeScript

**[paygate-sandbox](https://github.com/surakiartysk/paygate-sandbox)** · [live](https://paygate-sandbox.vercel.app)

A sandbox that emulates the 2C2P and Omise payment APIs, so an integration can
be tested against the responses a real staging environment will not produce on
demand: declines with a specific code, duplicate webhooks, out-of-order
callbacks, timeouts. Your backend is unchanged; a second API drives the outcome.

Node · Vercel

---

[LinkedIn](https://www.linkedin.com/in/surakiartysk/)
