# sonder-emails

Builds Gallery Sonder show emails and packages them for Mailchimp.

```
sonder-emails/
  CLAUDE.md                     house rules Claude follows here
  scripts/package_mailchimp_zip.sh   builds the clean Mailchimp import zip
  shows/<show>/
    catalogue/                  extracted catalogue data (from sonder-catalogue)
    closer-look/                the email (index.html + images)
```

Use: open this folder in Claude Code and ask, e.g. "Make the Closer Look email for this show, feature *Coral Stack*." Then ask it to package the email, and in Mailchimp go to Create → Email → Code your own → Import zip.
