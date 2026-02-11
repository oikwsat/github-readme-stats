Fixes #116

This PR addresses issue #116, which reported the public deployment being paused. The issue stems from changes in Vercel's OSS sponsorship, making the official `github-readme-stats.vercel.app` deployment uncertain.

To mitigate this, I've added important notices to `readme.md` and `docs/readme_ja.md`, informing users about the potential pause and strongly recommending deploying their own instance on Vercel for uninterrupted service.

No code changes were made to the core functionality, as the issue is related to deployment infrastructure rather than a bug in the application code.