# Learn React from scratch on macOS

## Step 1 - Setup

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
install node and npm
```sh
nvm install node
nvm install-latest-npm
```

Next, cd to the desired directory and create the project by
```sh
npx create-react-app my-app
cd my-app
npm start
```

Now one can see a default display at http://localhost:3000/


## Step 2 - Learn the basics

For some basic understandings, read through "Learn React in 10 tweets" (at https://twitter.com/chrisachard/status/1175022111758442497)
and an example (at https://twitter.com/chrisachard/status/1238491672851423234)

Then here's the practical tutorial to follow: https://reactjs.org/tutorial/tutorial.html

And try an exercise: https://gist.github.com/cybersiddhu/0a9147faff7378a40507a9a9815c4a2d


## Other good references
https://www.geeksforgeeks.org/reactjs-importing-exporting/


https://reactjs.org/docs/hooks-intro.html

https://daveceddia.com/usestate-hook-examples/

https://www.robinwieruch.de/react-remove-item-from-list
