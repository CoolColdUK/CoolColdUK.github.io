---
tags: npm
---
following will update to the latest minor version but not the major version due to breaking changes
> npm update

To update major version, use
> npm install -g npm-check-updates
> ncu -u
> npm update
where above will update to latest major version, then update to the latest minor version for both dependencies and devDependencies