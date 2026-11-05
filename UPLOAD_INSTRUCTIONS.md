# Uploading Boredum Busters to GitHub

There are two ways to do it. **Option A** needs only a web browser. **Option B** has Claude do the upload from another account.

---

## Option A: upload in the browser (about 5 minutes)

1. Sign in at **github.com** and click **New** (green button) to create a repository.
   - Repository name: `boredum-busters` (or any name)
   - Public or Private: your choice. GitHub Pages is free for public repos; private repos need a paid plan.
   - Leave **Add a README** unticked so the repo starts empty.
   - Click **Create repository**.
2. On the empty repo page, click **uploading an existing file**.
3. Unzip `boredum-busters-github.zip` on your computer. Open the `boredum-busters` folder, select **everything inside it** (`index.html`, `media`, `brand-kit`, `README.md`, `STRUCTURE.md`, `UPLOAD_INSTRUCTIONS.md`, `.gitignore`) and drag it onto the GitHub page.
   - Drag the contents, not the outer folder, so `index.html` ends up at the top of the repo.
   - `.gitignore` starts with a dot, so your file browser may hide it. It's optional; skip it if you can't see it.
4. Wait for all files to finish uploading. The largest is about 3 MB, well under GitHub's 25 MB browser limit. Then type a message such as `Initial upload` and click **Commit changes**.

## Option B: let Claude upload it from another account

In the other Claude account, start a session with GitHub access, attach `boredum-busters-github.zip`, and paste this prompt:

> I've attached `boredum-busters-github.zip`. Please:
> 1. Unzip it. The repository content is inside the `boredum-busters` folder.
> 2. Push everything in that folder (including `.gitignore`) to my GitHub repository **`YOUR-USERNAME/boredum-busters`** on the `main` branch, with `index.html` at the repository root. If the repository doesn't exist yet, tell me and I'll create it empty first.
> 3. Use the commit message: `Initial upload: Boredum Busters website and brand kit`.
> 4. Don't change any file contents.
> 5. When done, give me the repository link and remind me how to turn on GitHub Pages.

Replace `YOUR-USERNAME` with your GitHub username before sending.

---

## Turn on the free live website (GitHub Pages)

1. In the repository, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Set **Branch** to `main` and the folder to `/ (root)`, then click **Save**.
4. After a minute or two, the site is live at:
   `https://YOUR-USERNAME.github.io/boredum-busters/`

Each new commit to `main` updates the live site automatically.

---

## After uploading

- **Fill in the placeholders:** `[STUDIO EMAIL]`, `[STUDIO PHONE]`, `[@HANDLE]`, the three `[GAME TITLE]`s, the build `[XX]%` and the store links. The table in `README.md` lists them all. You can edit `index.html` directly on GitHub with the pencil icon.
- **Pitch form:** on GitHub Pages it doesn't store submissions. Connect it to a form service (Formspree, Basin, Google Forms) to receive pitches.
- **Large video masters:** the transparent ProRes 4444 loader files (about 60 MB and 96 MB) are left out on purpose to keep the repository light. Keep them in your Drive or the full brand-kit zip. If you ever need them in GitHub, use Git LFS.
- **Custom domain (optional):** in **Settings → Pages → Custom domain**, enter your domain, then add the DNS records GitHub shows you.
