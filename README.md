# Invitation Downloader

Two-page site: **enter full name** → **invitation page with auto-download**.  
The downloaded file is saved with the guest’s name (e.g. **jamesguestdetails.pdf**).

---

## Upload this folder to GitHub

1. Go to [github.com](https://github.com) → **New repository**.
2. Name the repo (e.g. `invitation` or `rsvp-invite`). Create it **without** a README.
3. Upload this whole folder:
   - Drag the **downloader-page** folder into the repo, or
   - Use **Upload files** and add everything inside **downloader-page** (index.html, download.html, README.md, and any images/file you add).

4. Add your **download file** (e.g. invitation.pdf or your .msi) in the **same folder** as index.html and download.html.
5. In **download.html**, near the top of the `<script>`, set:
   - `FILE_URL = 'invitation.pdf';`  (your file name)
   - `FILE_EXT = 'pdf';`  (or `'msi'` if you use .msi)

6. Turn on **GitHub Pages**:  
   **Settings** → **Pages** → **Source**: Deploy from branch → **main** → **/ (root)** → Save.

Your site will be at: **https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/**

---

## What’s in this folder

| File           | Purpose |
|----------------|--------|
| **index.html** | First page: “Find your invite”, full name, Continue. |
| **download.html** | Second page: “You’re invited”, Dear [Name], auto-download + manual link. |
| **README.md**  | This file. |

**You add:**

- Your **download file** (e.g. `invitation.pdf`) in this same folder.
- Optional: **Background images**  
  - First page: in **index.html** CSS, set `--bg-image: url('your-image.jpg');` (or `none` for gradient).  
  - Second page: in **download.html** CSS, set `background: url("your-image.jpg")` (or the page will use a gradient if the image is missing).

---

## How the download name works

If the user enters **James**, the file is saved as **jamesguestdetails.pdf**.  
If they enter **James Smith**, it’s **jamessmithguestdetails.pdf**.  
(Spaces and non-letters are removed; then `guestdetails` + your file extension is added.)
