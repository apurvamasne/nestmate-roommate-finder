# Nestmate

A roommate-matching app. You take a 12-question lifestyle quiz covering budget, cleanliness, sleep, pets, smoking, guests and more. Then you browse roommate profiles sorted by how compatible they are with you.

The whole app is one file, `index.html`. It doesn't need a build step or a server.

## Put it online with GitHub Pages

1. Sign in at github.com and click **New repository**. Name it `nestmate`, set it to **Public**, and click **Create repository**.
2. On the new repo's page, click **uploading an existing file**. Drag in `index.html` and this `README.md`, then click **Commit changes**.
3. Go to **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **main**, and folder to **/ (root)**. Click **Save**.
4. Wait a minute or two, then refresh the Pages settings screen. Your link will appear there:
   `https://YOUR-USERNAME.github.io/nestmate/`

Share that link with anyone.

## Run it on your computer

Double-click `index.html` to open it in your browser.

## How matching works

- Each answer is compared with the other person's answer. Closer answers score higher.
- Some questions count more than others. Smoking, pets, cleanliness and budget overlap matter most.
- Some answers are dealbreakers. If you want a smoke-free home and the other person smokes indoors, the match is capped at 40%. The same goes for "no pets" versus "has a pet", which is capped at 45%.
- You can change the questions and weights in the `Q` list near the top of the `<script>`.

## Current limits

- The 8 profiles in Discover are examples, stored in the `P` list in the script.
- A person's quiz answers and likes are saved only in their own browser, so visitors don't see each other.
- "Matched" is simulated: it shows when compatibility is 70% or higher.

To turn this into a real multi-user app, you need a backend, such as Firebase or Supabase, for three things:
- user accounts
- storing everyone's profiles
- recording real mutual likes and messages
