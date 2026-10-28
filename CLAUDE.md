# Gallery Sonder emails

This folder builds Gallery Sonder's show emails for Mailchimp. The person working here is Josh at Gallery Sonder. He's new to Claude Code, so explain in plain language and avoid jargon.

## Josh sends by hand, always

You build and package the email. Josh imports it into Mailchimp, tests it and sends it himself. Never try to send or schedule anything.

## Copy

- Artist and gallery copy (press text, statements, captions) is reproduced word for word. Keep the original punctuation and spacing, and don't add curly quotes. Only edit it when Josh asks.
- Work details (title in italic, year, medium, dimensions in inches and cm, price) come from `shows/<show>/catalogue/catalogue.json`. That data is produced in the `sonder-catalogue` folder from the pre-catalogue PDF. For a new show, copy its `catalogue/` folder in here first.

## Emails

- Each show gets a folder: `shows/<show>/` with `catalogue/` (input, copied from `sonder-catalogue`) and one folder per email (`closer-look/`, `opening/`, ...).
- `shows/euphorbia/closer-look/` is the reference design: SONDER wordmark, the catalogue cover, the two-column info block, outlined buttons, catalogue-style work captions, the image credit line, and the standard footer.
- Every link to gallerysonder.com gets `utm_source=mailchimp&utm_medium=email&utm_campaign=<show>-<email>`, plus `utm_content=<work-slug>` on work links. Leave mailto and external links untagged.
- Package with `scripts/package_mailchimp_zip.sh <email-folder> <output>_MAILCHIMP.zip`. Never zip a whole folder by hand, because Mailchimp may pick up the wrong HTML file.
- Preview the email in a browser at desktop and phone width before packaging.
