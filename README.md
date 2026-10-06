# SafeSend Cloud

This is the basic cloud version. It uses Supabase Storage and does not require a login.

## Setup

1. Create a free Supabase project.
2. In **Storage**, create a bucket named `shares` and make it public.
3. Copy `config.example.js` to `config.js`.
4. Put the Supabase project URL and anon key in `config.js`.
5. Publish the `cloud` folder using GitHub Pages, Cloudflare Pages, or any static host.

The browser encrypts every file with AES-256-GCM before upload. Supabase receives only encrypted data. The password is never uploaded.

The basic version supports files up to 100 MB. Uploaded objects remain in storage until manually deleted from Supabase.
