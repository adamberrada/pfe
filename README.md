# pfe

Easy way to upload your React app + backend in this repo.

## 1) Use this folder structure

```text
pfe/
  frontend/   # React app
  backend/    # API/server
```

## 2) Copy your existing projects

From this repository root:

```bash
mkdir -p frontend backend
rsync -a --exclude node_modules --exclude dist --exclude build /path/to/your/react/ frontend/
rsync -a --exclude node_modules --exclude dist --exclude build /path/to/your/backend/ backend/
```

If `rsync` is not available (for example on some Windows setups), copy the folders manually into `frontend/` and `backend/`.

## 3) Commit and push

```bash
git add frontend backend .gitignore README.md
git commit -m "Add frontend and backend projects"
git push
```

## Optional: start both locally

```bash
# Terminal 1
cd frontend && npm install && npm run dev

# Terminal 2
cd backend && npm install && npm run dev
```

If your project uses different scripts/tools (`npm run start`, `yarn`, `pnpm`, etc.), use your existing commands instead.
