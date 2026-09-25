# famtest.lazzurs.ie

Throwaway GitHub Pages site for the Family Chat staging migration rehearsal
(unicornops/family-chat#237). `famtest.lazzurs.ie` is the custom domain a
seeded staging family migrates to, so its Matrix well-known files delegate
to that family's new staging instance.

The files permanently delegate to `stg-famtest.familychat.dev`. The
rehearsal pins the new staging instance to that host
(`start_homeserver_migration --serving-hostname`), so the files never change
per run and CI needs no access to this repo. Nothing here is production:
never point a real family at this domain.

`.nojekyll` is required, otherwise Jekyll skips the `.well-known` directory.
DNS lives in neamh/octodns (`config/lazzurs.ie.yaml`, `famtest` CNAME).
