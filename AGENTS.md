# Working in this repo

This is a teaching template for people who have never used GitHub. Someone clicks "Use this
template", edits one file in the browser, and gets a live site with a working contact form. Keep it
that way.

## The constraints that define this repo

- **No build step, no package manager, no terminal.** Everything must work when the reader edits
  files through GitHub's web editor and GitHub Pages serves the repo root as-is. Do not add
  `package.json`, a bundler, a framework, or a Pages build workflow.
- **One page.** `index.html` is the whole site. If a change needs a second file to make sense, it
  probably belongs in a different template.
- **Tailwind via the browser CDN**, loaded from `@tailwindcss/browser@4`. This is the one place in
  the org where the CDN build is correct, because the reader has no way to run a build. Style with
  utility classes, and put the theme in the `@theme` block so a beginner changes three colours in
  one place rather than hunting through markup.
- **Comments in `index.html` are the lesson**, not clutter. Keep `CHANGE ME` markers where the
  reader is meant to edit, and keep them rare enough to still mean something.

## The form

The `action` ships as the literal placeholder `https://f.bootform.com/__YOUR_FORM_ID__`.

**Never replace it with a real form ID.** A form ID is the entire claim credential: whoever claims
one first owns it permanently, and every fork then delivers its visitors' messages to that person.
An unclaimed ID also exposes held submissions to anyone who reads the repo. The reader generates
their own in step 4 of the README. This is not negotiable and is not a placeholder-for-convenience.

The honeypot input must stay. It is hidden, unlabelled to screen readers, and filtering depends on
it being submitted empty.

## Writing style

- Second person, present tense, short sentences. The reader is nervous and has not done this before.
- Say what will happen before asking them to click something, and say what they should see after.
- **No em dashes or en dashes.** Use a comma, a colon, a full stop, or brackets.
- No AI attribution in commits or pull requests, here or anywhere else in this organisation.
- Never claim BootForm offers EU data residency, a DPA, or an uptime SLA. It does not.

## Before changing anything

Read it as someone who has never made a website. If a step assumes knowledge the previous steps did
not give, that is a bug, and it is the most important kind of bug in this repo.
