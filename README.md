# tsconfig-index-bleed
Simple IDEA project that demonstrates [WEB-47435](https://youtrack.jetbrains.com/issue/WEB-47435),
i.e. effects of typescript configuration in a subdirectory bleeding outside it and affecting code assist
symbol resolution in unrelated files.

To reproduce:

1. VCS -> Get from Version Control -> GitHub -> rulatir/tsconfig-index-bleed (or fork on GitHub
beforehand if it would only work with a repo you own).
2. Settings... -> Languages & Frameworks -> Node.js and NPM -> Coding assistance
for Node.js. Don't define any scopes.
3. Open `apps/node-app/index.js` and behold the squiggle under `write`.
4. Rename `apps/ts-app/tsconfig.json` to `tsconfig.jsoff` to see the squiggle gone.

EDIT 2021-01-03: The issue has been declared fixed and is expected to land sometime during the 2020.3 era.
