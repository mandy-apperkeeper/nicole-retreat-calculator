# Deploy to apperkeeper.com — Step by Step

## Delete the Worker you accidentally created

1. Go to `dash.cloudflare.com`
2. Left sidebar: click **Workers & Pages**
3. Find the `nicole-retreat-calculator` worker you created
4. Click on it → **Settings** → scroll to bottom → **Delete**
5. Confirm deletion

## Create a Pages project (correct way)

1. Go to `dash.cloudflare.com`
2. Left sidebar: click **Workers & Pages**
3. Click **Create** button (top right area)
4. You'll see tabs: click **Pages**
5. Click **Connect to Git**
6. If prompted, authorize Cloudflare to access your GitHub (mandy-apperkeeper account)
7. You'll see a list of your repos — select **nicole-retreat-calculator**
8. Click **Begin setup**

## Configure build settings

9. **Project name**: `nicoleretreat` (this affects the .pages.dev URL)
10. **Production branch**: `master`
11. **Framework preset**: None
12. **Build command**: leave BLANK (empty)
13. **Build output directory**: leave BLANK (or type `/` if it won't let you leave it empty)
14. Click **Save and Deploy**

## Wait for deploy

15. It'll show build logs for ~30 seconds
16. When done, you'll see a green checkmark and a URL like: `nicoleretreat.pages.dev`
17. Click that URL — you should see the calculator at `/nicoleretreat` path

## Add custom domain (apperkeeper.com)

18. On your project page, click the **Custom domains** tab
19. Click **Set up a custom domain**
20. Type: `apperkeeper.com`
21. Click **Continue**
22. Since the domain is already on your Cloudflare account, it should verify automatically (no DNS changes needed)
23. Click **Activate domain**
24. Wait 1-2 minutes

## Done

The calculator should now be live at:
- `apperkeeper.com/nicoleretreat`

Every time changes are pushed to the GitHub repo, Cloudflare auto-deploys within ~30 seconds.
