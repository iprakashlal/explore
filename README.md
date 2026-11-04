# Prakash Lal · Portfolio

A single-page geometric portfolio with its own control panel. Everything runs on GitHub Pages: content is stored in `content.json`, images in `assets/uploads/`, and the panel saves by committing to this repository.

## Files
| File | What it is |
|---|---|
| `index.html` | The site and the control panel (open `/#admin`) |
| `content.json` | All site text, colours, shapes and image paths |
| `auth.json` | Created by the panel on first setup. Holds your GitHub token, encrypted with your panel password |
| `assets/uploads/` | Images uploaded from the panel |
| `geometry.html`, `blueprint.html` | Earlier design variants |

## First-time setup
1. Create a fine-grained token: GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token.
   - Repository access: **Only select repositories** → this repository.
   - Permissions → Repository permissions → **Contents: Read and write**.
2. Open `https://<username>.github.io/<repo>/#admin`.
3. Fill in the setup form: repository details, the token, and the username and password you want for the panel.

## Editing
Sign in at `/#admin`, edit, then press **Save & publish**. GitHub Pages republishes in about a minute.

## Forgot the password or token expired
- Token expired: sign in and add a new token under **Account & login**.
- Forgot password: delete `auth.json` from the repository, wait a minute, open `/#admin` and set up again. Your content is untouched.

## Security
Your token is only ever stored encrypted. `auth.json` is public, so use a long, unique panel password, and limit the token to this one repository.
