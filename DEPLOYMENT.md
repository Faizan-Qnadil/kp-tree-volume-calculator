# Publish through PFI GitHub and Cloudflare Pages

## 1. Repository ownership

The repository is owned and controlled by Faizan-Qnadil:
https://github.com/Faizan-Qnadil/kp-tree-volume-calculator

The repository is public. PFI branding and scientific attribution do not change account ownership. Use your own Cloudflare account to retain hosting control as well. The application files are in dist/; deploy only that directory. No credentials are required in the repository.

## 2. Connect Cloudflare Pages to GitHub

In Cloudflare: Workers & Pages → Create application → Pages → Connect to Git. Authorize the PFI repository, select it, and configure:

| Setting | Value |
| --- | --- |
| Production branch | main |
| Framework preset | None |
| Root directory | Repository root (leave default) |
| Build command | Leave blank |
| Build output directory | dist |
| Environment variables | None required |

Choose Save and Deploy. Record the actual assigned pages.dev address; no address is reserved by this package. Future pushes to the production branch automatically deploy, so review equation changes before merging to main.

Official instructions: https://developers.cloudflare.com/pages/get-started/git-integration/
Static HTML: https://developers.cloudflare.com/pages/framework-guides/deploy-anything/

## 3. Validate the new site

- Open the assigned HTTPS address on an Android phone and a desktop browser.
- Compare several single-tree results against the current calculator, including unit changes and range boundaries.
- Import a small inventory, check exclusions and totals, export CSV/Excel and print a report.
- Wait for Ready for offline use, enable flight mode, reopen the same address and calculate again.
- Save a JSON backup and restore it in the new site. Check tree counts and totals.

The package retains the existing application logic. Packaging checks verify unchanged equation files and complete offline assets; actual Cloudflare deployment and device/offline checks remain to be completed.

## 4. Establish the permanent public address

Start with Cloudflare's assigned pages.dev address. PFI's IT administrator can later add an approved institutional subdomain in the project's Custom domains settings and configure the required DNS records. Pick the permanent address before broad distribution so users do not have to move device-saved inventories repeatedly.

The guide now shares the address from which it is opened. Its old QR code has been removed from this migration copy because it pointed at the ChatGPT-hosted site. Generate a new QR code after the permanent address is confirmed and add it to the guide and offline cache list.

## 5. Move users safely

Keep the old site available during transition. Each user should open the old site on the same device/browser that holds their records, export a JSON backup, open the new site, restore it and check totals. Saved data and offline installation do not transfer automatically between website addresses. Install/bookmark the new site and repeat the flight-mode test. Cloud hosting does not introduce shared inventories or synchronization.

The current ChatGPT site is not changed or unpublished by preparing this package.
