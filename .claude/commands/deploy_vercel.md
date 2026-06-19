# Deploy to Vercel

Deploy this project to Vercel production.

## Steps

1. Make sure the project builds successfully first:
   ```bash
   npm run build
   ```

2. If Vercel CLI is not installed, install it:
   ```bash
   npm install -g vercel
   ```

3. If not logged in to Vercel, authenticate first:
   ```bash
   vercel login
   ```

4. Deploy to production:
   ```bash
   vercel --prod --yes
   ```

5. The deployment URL will be printed in the terminal output. Share it with the user.

## Notes

- The `build/` output directory is configured in `vite.config.ts` (`outDir: 'build'`).
- Vercel will auto-detect this as a Vite project.
- Use `vercel --prod --yes` to skip interactive prompts and deploy directly to production.
- If this is the first deploy, Vercel may ask for project name and scope — answer interactively or use `--name` and `--scope` flags.