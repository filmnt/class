May it be of help to those dedicated to the realm of education...

# Getting Started

```shell
git clone https://github.com/filmnt/class.git
cd class
rm -rf node_modules package-lock.json
npm install
npx quartz build --serve
```
> Modify `quartz.config.ts` with VS Code

Connect `localhost:8082`

# Web-Publish
Install <a href="https://nodejs.org/en" target="_blank" >Node</a>, <a href="https://code.visualstudio.com/download" target="_blank" >VS Code</a>, <a href="https://desktop.github.com/" target="_blank" >GitHub Desktop</a> 

Create Github-Repository

`Settings` - `Pages` -> Under `Source`, select `GitHub Actions`

```shell
cd class
git remote rm origin
git remote add origin <https://Your-Repository.git>
```

Open Github-Desktop and Add `class`, `commit and push` 

This should deploy your site to <github-username>.github.io/<repository-name> like `filmnt.github.io/class`
> ShortUrl -> `repository-name` -> `<username>.github.io`