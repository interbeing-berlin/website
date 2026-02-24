# interbeing.berlin

Website for a Church of Interbeing, Berlin. Built with [Jekyll](https://jekyllrb.com/) and hosted on GitHub Pages.

## Setup

### 1. Configure integrations

Edit `_config.yml` and fill in:

- **`behold_feed_id`** — Sign up at [behold.so](https://behold.so), connect the `church_of_interbeing` Instagram account, create a widget, and paste the feed ID here.
- **`mailchimp_u`** and **`mailchimp_id`** — In Mailchimp, go to Audience → Signup forms → Embedded forms. In the generated form code, find the `action` URL which looks like:
  ```
  https://us22.list-manage.com/subscribe/post?u=XXXXXXXXXXXX&id=YYYYYYYYYY
  ```
  Copy the `u=` value into `mailchimp_u` and the `id=` value into `mailchimp_id`.
- **`google_calendar_id`** — Already set to `info@interbeing.life`. Make sure this calendar is set to public in Google Calendar settings (Settings → calendar → Access permissions → Make available to public).

### 2. Set up GitHub Pages

1. Go to repo Settings → Pages
2. Set source to `main` branch, root folder
3. The `CNAME` file is already present for `interbeing.berlin`

### 3. Configure DNS

Add these DNS records for `interbeing.berlin`:

| Type  | Name | Value               |
|-------|------|---------------------|
| A     | @    | 185.199.108.153     |
| A     | @    | 185.199.109.153     |
| A     | @    | 185.199.110.153     |
| A     | @    | 185.199.111.153     |

GitHub will auto-provision HTTPS.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Site will be available at `http://localhost:4000`.

## Editing content

All pages are Markdown files in the root directory. Edit them directly on GitHub or locally:

- `index.md` — Home / About page
- `calendar.md` — Calendar page
- `email-list.md` — Email signup page

Site config (title, links, integration IDs) is in `_config.yml`.
