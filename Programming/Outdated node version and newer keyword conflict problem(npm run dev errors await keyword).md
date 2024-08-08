## Outdated node version and newer keyword error

### Error:

<code>node_modules/vite/bin/vite.js:7
await import('source-map-support').then((r) => r.default.install())
^^^^^
SyntaxError: Unexpected reserved word
at Loader.moduleStrategy (internal/modules/esm/translators.js:133:18)
at async link (internal/modules/esm/module_job.js:42:21)</code>

### Explanation:

The error I was encountering typically arises from trying to run code that uses modern ECMAScript features in an environment that doesn't fully support them. In this case, the issue seems to be with the use of the await keyword at the top level, which is part of the ECMAScript module syntax introduced in more recent versions of Node.js.

### Solve:

1. Check Node.js Version:
   <code>node -v</code>
2. If the version is outdated, you can update Node.js to the latest LTS version. You can use tools like nvm (Node Version Manager) to manage and switch between Node.js versions:
   <code>nvm install --lts\
   nvm use --lts
   </code>
3. If nvm (Node Version Manager) is not installed on your system, You'll need to install nvm before you can use it to manage Node.js versions.\

- Download and Install nvm:
  <code>curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
  </code>
- Activate nvm:
  <code>source ~/.bashrc</code>
- Verify nvm Installation:
  <code>nvm --version</code>\
  If it does not shows the version name, that means it is not properly installed, redo the step 3 again.

4. Redo step 2 again.
5. Reinstall Project Dependencies: \
   Remove the node_modules folder and reinstall.\
   <code>rm -rf node_modules\
   npm install
   </code>
6. Now run the <code>npm run dev</code> command.

#### If the issue presists:

1. Verify Node.js Version in Use: <code>node -v
   </code>
2. Check for Multiple Node.js Installations: <code>which node
   </code>
3. Update Vite: <code>npm install vite@latest --save-dev
   </code>
4. Update npm: <code>npm install -g npm
   </code>

Now you will be able run the project after applying the solve.

Happy Coding!!!
