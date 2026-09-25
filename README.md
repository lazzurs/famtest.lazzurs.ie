# famtest.lazzurs.ie

Throwaway GitHub Pages site for the Family Chat staging migration rehearsal
(unicornops/family-chat#237). `famtest.lazzurs.ie` is the custom domain a
seeded staging family migrates to, so its Matrix well-known files must point
at the new instance's generated serving hostname for that run.

The staging test rewrites both files through the GitHub contents API at the
start of the rehearsal and resets them to `{}` afterwards. Nothing here is
production: never point a real family at this domain.

`.nojekyll` is required, otherwise Jekyll skips the `.well-known` directory.
DNS lives in neamh/octodns (`config/lazzurs.ie.yaml`, `famtest` CNAME).
