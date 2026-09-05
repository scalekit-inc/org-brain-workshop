# Fix: cron alerting + TLS renewal lead time

- Corrected the log rotation cron's path (broken by a prior infra migration) and added alerting on cron failure itself, not just downstream symptoms.
- Extended TLS certificate renewal alert lead time from 3 to 21 days, with escalating alerts at 21/7/3 days.
