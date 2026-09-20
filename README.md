# Your first website, in about 15 minutes

No installs. No terminal. No account anywhere, until the very last step, and even then only if you
want to keep what people send you.

By the end you will have a real page at `https://yourname.github.io/first-website`, with a contact
form that genuinely sends you the messages.

**[See what you are building →](https://bootform.github.io/first-website/)**

---

## Before you start

You need a free GitHub account. That is it. If you are reading this, you may already have one.

Everything below happens in your browser.

---

## Step 1: Make your own copy

Click the green **Use this template** button at the top of this page, then **Create a new
repository**.

Name it `first-website`. Leave everything else alone and click **Create repository**.

You now have your own copy. Nothing you do from here can break the original.

---

## Step 2: Put it on the internet

In *your* new repository:

1. Click **Settings** (the tab along the top).
2. Click **Pages** in the left sidebar.
3. Under **Source**, choose **Deploy from a branch**.
4. Set the branch to **main** and the folder to **/ (root)**. Click **Save**.

Wait about a minute, then reload that Settings page. A green box appears at the top with your
address, something like `https://yourname.github.io/first-website/`.

**Open it.** That is your website. It is live, on the real internet, and anyone can visit it.

It still says Sam Rivera. We will fix that next.

> **If you get a 404:** give it another minute or two. The first build is the slow one.

---

## Step 3: Make it yours

Back on your repository's main page, click **`index.html`**, then click the pencil icon (✏️) to
edit it.

Look for the lines marked `CHANGE ME`. There are two:

- **The title**, near the top. This is what shows in the browser tab.
- **Two colours**, just below it. `--color-ink` is the text, `--color-paper` is the background,
  `--color-accent` is the buttons and links.

Then change the actual words on the page: the name in the big heading, the paragraph under it, the
two things under "What I do".

When you are done, click **Commit changes...** at the top right, then **Commit changes** in the box
that appears.

Wait a minute, reload your site, and it is yours.

> **Picking colours is the hard part.** If you have no idea, try `--color-paper: #0f1115` and
> `--color-ink: #e8e6e1` for a dark version, and pick any accent you like.

**Optional: use your own photo.** The page starts with a demo photo so you can see how it looks.
To swap in your own:

1. On your repository's main page, click **Add file → Upload files**.
2. Drag in your photo and name it exactly `sample-profile-photo.jpg`. Uploading a file with the
   same name replaces the one that's there.
3. Commit the upload.
4. Edit `index.html`, find the `<img src="sample-profile-photo.jpg" ...>` line near the top, and
   change `alt="Sam Rivera"` to your own name.

Don't want a photo at all? Delete the `<img>` line (and the `CHANGE ME` comment above it) and the
page still works, just without one.

**Optional: add your links.** Just below your bio is a row of links marked `CHANGE ME: your links`.
Each one is a single line, for example:

```html
<a href="https://instagram.com/yourname" class="underline decoration-ink/25 underline-offset-4 hover:text-accent hover:decoration-accent">Instagram</a>
```

Change the address in `href` to your own, change the text between the tags to whatever you want it
to say, and delete any line you don't want. Copy a line and change both to add one that isn't there
already, like a Bluesky profile or your own site.

---

## Step 4: Make the contact form actually work

Here is the bit most tutorials skip.

Your page is a *static* site. There is no program running behind it, so there is nowhere for a form
to send anything. That is why every "build a website" tutorial stops at a form that looks right and
does nothing.

You need somewhere for the message to go. We will use [BootForm](https://bootform.com), because you
can point a form at it and it works immediately, with no account.

**4a. Generate your form ID.**

It is just a random UUID, and it has to be yours alone. Pick any one of these:

- Open BootForm's own [UUID generator](https://bootform.com/uuidgenerator) and copy what it shows
  you. Nothing you generate there is sent anywhere; it runs entirely in your browser.
- Or paste this into your browser's address bar and press enter:
  `javascript:prompt("Your form ID", crypto.randomUUID())`
- Or, on any page, open the browser console (F12) and run `crypto.randomUUID()`.

You will get something like `11111111-1111-4111-8111-111111111111`, though a real one won't repeat
digits like that; a genuine random UUID looks far more scrambled.

> **Use your own.** Do not use the one printed above, and do not use a friend's. Whoever claims a
> form ID first owns it, and everything sent to it goes to them. Yours should be a fresh random one
> that nobody else has seen.

**4b. Paste it in.**

Edit `index.html` again. Find this line:

```html
<form action="https://f.bootform.com/__YOUR_FORM_ID__" method="POST" class="flex flex-col gap-5">
```

Replace `__YOUR_FORM_ID__` with your ID, so it reads:

```html
<form action="https://f.bootform.com/11111111-1111-4111-8111-111111111111" method="POST" class="flex flex-col gap-5">
```

Commit the change. Wait a minute.

**4c. Try it.**

Go to your live site, fill in the form, and send it.

You will land on a page that says the message is being held, and asks you to claim the form. That is
the point: it accepted your message before you had an account anywhere.

**4d. Claim it.**

Click the claim link and create a free account. Everything already sent to your form is delivered to
you straight away.

From now on, anything anyone sends through your site arrives in your inbox.

> **Don't leave it too long.** Held messages are kept for 48 hours before they are deleted. Claim
> the form the same day you put it live.

---

## That's it

You have a live website with a working contact form, and you did it without installing anything.

### Where to go next

| | |
|---|---|
| **A proper domain** | `yourname.com` instead of `github.io`. GitHub's own guide: [managing a custom domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site). |
| **More pages** | Copy `index.html` to `about.html` and link to it. That is genuinely all it takes. |
| **A bigger site** | [vitepress-marketing](https://github.com/BootForm) when you want a blog and several pages that share a design. |
| **More form options** | File uploads, autoresponders, Discord and Slack: [bootform.com/docs](https://bootform.com/docs/). |

### Stuck?

Open an [issue](https://github.com/BootForm/first-website/issues) and say what happened. There is no
such thing as a question that is too basic here. That is what this repo is for.

---

## Frequently hit problems

**My site shows a 404.** The first build takes a few minutes. If it has been longer, check Settings
→ Pages still says branch `main` and folder `/ (root)`.

**My changes aren't showing.** Each commit triggers a rebuild that takes about a minute. If it still
looks old after that, hard-reload the page: `Ctrl+Shift+R`, or `Cmd+Shift+R` on a Mac.

**The form shows raw text instead of a nice page.** You are seeing the response as JSON. That is
normal for now. Once you claim the form you can set a redirect so people land back on your site.

**"This form has reached its limit of 10 held submissions."** You tested it more than ten times
before claiming. Claim the form and the limit goes away.

## Licence

MIT. Do whatever you like with it, including using it for a real business.
