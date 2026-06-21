# Deploy to GitHub Pages

Deploy this project to GitHub Pages.

## Steps

1. Run the deploy script (builds and publishes to the `gh-pages` branch):
   ```bash
   npm run deploy
   ```

2. The deployment URL will be: `https://<username>.github.io/<repo-name>/`
   Share the URL with the user.

## Notes

- `npm run deploy` runs `npm run build && gh-pages -d build` automatically.
- The `build/` output directory is configured in `vite.config.ts` (`outDir: 'build'`).
- GitHub Pages serves from the `gh-pages` branch. It may take 1-2 minutes to propagate after publishing.
- The site URL follows the pattern: `https://<github-username>.github.io/<repository-name>/`