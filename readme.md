
### Step-by-step Instructions ([Hugo Documentation](https://gohugo.io/hosting-and-deployment/hosting-on-github/))

- Create a `<YOUR-PROJECT>` (e.g. blog) repository on GitHub. This repository will contain Hugo's content and other source files.
- Create a `<USERNAME>.github.io` GitHub repository. This is the repository that will contain the fully rendered version of your Hugo website.

- `git clone <YOUR-PROJECT-URL> && cd <YOUR-PROJECT>`

- Paste your existing Hugo project into a new local `<YOUR-PROJECT>` repository. Make sure your website works locally (`hugo server` or `hugo server -t <YOURTHEME>`) and open your browser to http://localhost:1313.

- Once you are happy with the results:
  - Press Ctrl+C to kill the server
  - Before proceeding run rm -rf public to completely remove the public directory

- `git submodule add -b master git@github.com:<USERNAME>/<USERNAME>.github.io.git public`. This creates a git submodule. Now when you run the hugo command to build your site to public, the created public directory will have a different remote origin (i.e. hosted GitHub repository).

- From now on run `deploy.sh` to deploy

### Running Locally

```sh
hugo server -D
```

### Building

```sh
hugo
```

### Deploy
```
bash deploy.sh
```