# everbox

```clojure
(def everbox (combine evernote dropbox))
```

Evernote is a very useful, handy note taking software. And it also has many
wonderful GUI clients, you make some change, it auto-sync to the evernote server.
But as a software engineer, we used to editing files using Emacs/VIM rather than
using GUI clients, so `everbox` let you edit the files directly using your
favorite editor(Emacs!!), and it also auto-sync your changes to evernote server
(Just like dropbox).

It is still under developing.

## Config

You need to put the following config in `~/.everbox/everbox.yaml`
Sandbox:
```yaml
dev-token: "your-sandbox-developer-token"
user-store-url: "https://sandbox.evernote.com/edam/user"
everbox-root: "/path/to/store/your/evernote"
```
Production:
```yaml
dev-token: "your-production-developer-token"
user-store-url: "https://www.evernote.com/edam/user"
everbox-root: "/path/to/store/your/evernote"
```

## Usage

```bash
git checkout https://github.com/xumingming/everbox.git
cd everbox
lein run setup # fetch the content from evernote for the first time
lein run sync  # monitor the local changes
```
## FAQ
### Why there is a folder named maven_repo?
    http://www.pgrs.net/2011/10/30/using-local-jars-with-leiningen/

### Why not using the standard version of thrift?
    http://discussion.evernote.com/topic/27805-evernote-libthrift

### How to get an evernote developer token?
for sandbox:
```html
    https://sandbox.evernote.com/api/DeveloperToken.action
```
for production:
```html
    https://www.evernote.com/api/DeveloperToken.action
```

## License

Copyright © 2012 [@xumingming](https://github.com/xumingming)

Distributed under the Eclipse Public License, the same as Clojure.
