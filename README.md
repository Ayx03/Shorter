# :link: Shorty

Short chain generator: a serverless service built on vercel

## Online Services

- https://nb.js.cn/

## Deploy with Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2Fzce%2Fshort&env=GITHUB_OWNER,GITHUB_REPO,GITHUB_ISSUE_ID,GITHUB_TOKEN&demo-url=https%3A%2F%2Ft.zce.me)

### Environment Variables

- `REDIS_URL`: Redis url.
- `GITHUB_OWNER`: GitHub repo owner.
- `GITHUB_REPO`: GitHub repo name.
- `GITHUB_ISSUE_ID`: GitHub repo issue id for storage.
- `GITHUB_TOKEN`: GitHub access_token with `repo` scope.

> Tips. Using a closed & locked issue will be more reliable.
> `REDIS_URL` isn't required if you use a GitHub issue as the database.

## Endpoints

### GET `/create`

Create a new short url.

```shell
$ curl https:///create -d "url=https://yesmore.cc" -d "slug=xxx"
```

#### Parameters

- `url`: target url
- `slug`: short slug, default: `auto nanoid`

#### Response Type

```json
{
  "slug": "<slug>",
  "link": "https://nb.js.cn/<slug>"
}
```

## License

[MIT](LICENSE) &copy; [yesmore](https://yesmore.cc)
