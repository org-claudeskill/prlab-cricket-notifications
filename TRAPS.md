# Traps for single-repo review

## `trap/notify-on-display`

**The PR:** fans missed appeals. Push when `last_event.display` is `WICKET` or `NOT_OUT`, not only when `wicket_counted` is true.

**What a hop-2 review usually says:** better engagement, uses scoring's own label, tests added, LGTM.

**1 hop up (scoring):** `wicket_counted` is the dismissal signal. `NOT_OUT` means the appeal failed.

**Functional truth:** a push titled WICKET for an appeal that was not given is a wrong scorecard, not a feature.
