## 2026-04-17 - [Intl.DateTimeFormat Caching]
**Learning:** Initializing Intl.DateTimeFormat is extremely expensive (approx 250x slower than reusing a cached instance). toLocaleString() initializes a new formatter on every call.
**Action:** Always use cached Intl.DateTimeFormat instances for repeated date/number formatting in performance-sensitive paths like timeline rendering or search results.
