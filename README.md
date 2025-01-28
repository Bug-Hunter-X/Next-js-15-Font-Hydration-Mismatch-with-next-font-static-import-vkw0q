# Next.js 15 Font Hydration Mismatch

This repository demonstrates a bug and its solution related to font hydration mismatches in Next.js 15 when using the `next/font` module with `static` import.  The issue arises from inconsistencies between server-side rendering (SSR) and client-side hydration, leading to missing or incorrectly rendered fonts.

## Bug
The `font-hydration-bug.js` file showcases the problematic implementation where the `static` import of fonts results in a hydration mismatch. The fonts render correctly on the server but fail to hydrate correctly on the client.

## Solution
The `font-hydration-solution.js` file provides a corrected implementation which ensures correct font loading and hydration on both server and client.  This might involve verifying proper font file serving, caching, and potentially using a different font loading method if `static` import continues to present problems. 

## Reproduction
1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Observe the font rendering on the page.  The bug version will show a mismatch, while the solution version will render correctly.