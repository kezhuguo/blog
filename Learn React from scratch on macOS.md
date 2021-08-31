# Learn React from scratch on macOS

## Step 1

Start by installing the version manager nvm for node.js

(Following https://github.com/nvm-sh/nvm#installing-and-updating and https://create-react-app.dev/docs/getting-started)

run in kernel:
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```
then I had to manually add the source lines to the profile file
```sh
open .bash_profile
```
in the opened file, add
```sh
# manually added for nvm
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```
then run to verify installation
```sh
command -v nvm
```

Next, create the project by
```sh
npx create-react-app my-app
cd my-app
npm start
```






```sh

```



