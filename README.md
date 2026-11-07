# F-16 Airframe Explorer

An interactive 3D model of the F-16C Block 50. Click any of 21 components to see its specifications, the engineering behind it, how it fails, and a student-level project to try. A performance tab computes wing loading, drag, stall speed and turn performance live.

## Run locally

Open `index.html` in a browser. It loads three.js and fonts from a CDN, so it needs an internet connection. To serve it over HTTP instead: `npx serve .`

## Deploy

1. Push this folder to a GitHub repository.
2. In Vercel choose Add New, then Project, and import the repository.
3. Framework Preset: Other. Leave the build command and output directory empty.
4. Deploy. Every later push to the main branch redeploys, and every pull request gets a preview URL.

## Data and accuracy

Every number in the inspector carries a tag: Verified, Varies, Derived, Model, or Not verified. Sources are linked inside the app (Sources tab). The geometry is generated in code from published overall dimensions. Fuselage cross-sections, tail sizes and component positions are estimates, tagged Model. This is not CAD or manufacturer data.

## Stack

Plain HTML, CSS and JavaScript with three.js r128 from cdnjs. No build step.

## Ideas for next steps

- Vendor three.js into the repository so the site has no CDN dependency.
- Replace the estimated planform with your own XFLR5 or OpenVSP geometry and compare lift slopes with the calculator.
- Add a second aircraft by moving the part data to JSON files.
