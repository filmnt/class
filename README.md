May it be of help to those dedicated to the realm of education...

# Getting Started

```shell
git clone https://github.com/filmnt/class.git
cd class
rm -rf node_modules package-lock.json
npm install
npx quartz build --serve
```
Connect `localhost:8082`

# Web-Publish
`Settings` - `Pages` -> Under `Source`, select `GitHub Actions`

This should deploy your site to <github-username>.github.io/<repository-name> like `filmnt.github.io/class`
> ShortUrl -> `repository-name` -> `<username>.github.io`