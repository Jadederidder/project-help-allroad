# Email artwork

The artwork used in the AllRoad welcome emails, kept here because this repo is
public and `raw.githubusercontent.com` therefore serves it without a credential.

That matters for one reason: it is how the bytes get into the `collateral`
bucket without a human uploading anything. `ph-image-stage` fetches a URL and
writes it to the bucket, so artwork that exists only on a workstation needs a
public URL to be fetched FROM. Joomla provided that for everything already on
the old site; this folder provides it for everything new.

The customer never sees these URLs. Delivery is still
`premiumhelp.co.za/i/<name>` off the Cloudflare Worker, reading the bucket.

| File | Size | Used by |
|---|---|---|
| `vw-header.jpg` | 440x231 | `welcome-email-vw-*` |
| `audi-header.jpg` | 480x252 | `welcome-email-audi-*` |
| `allroad-footer.jpg` | 580x260 | both welcome emails |

The header slot in the template is declared 580x280, so both headers are
currently upscaled by roughly a third and will look soft. Artwork at 580px
wide is the real fix; it has not been done.

Images only. Never code, credentials or customer data.
