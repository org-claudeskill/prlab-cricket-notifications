# cricket-notifications (hop 2)

Push alerts. **Two hops** from `cricket-protocol`. **One hop** from `cricket-scoring`.

Sends only when `last_event.wicket_counted` is true. Does not parse `display`, `extras`, or `umpire_confirmed`.

A protocol default that makes scoring count an unconfirmed LBW sends a "WICKET" push from this service without this file changing.

## Trap branch

`trap/notify-on-display` — also push when `display == "WICKET"` or `display == "NOT_OUT"` so fans do not miss appeals. Tests stay green. Unconfirmed LBWs page the user.

## Develop

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -e ".[dev]"
pytest
```
