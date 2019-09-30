# `now dev` not rendering custom error pages

## Development

Run `yarn dev` (or `next`) to test locally. Navigate to [`http://localhost:3000/asdf`](http://localhost:3000/asdf) to see a 404. Logs should read:

```
Error rendered: 404; Url: /asdf; IP: ::1
```

## Test locally

Run `now dev`, then open [`http://localhost:3000/asdf`](http://localhost:3000/asdf). You'll see the `now dev` error page, and no logging.

## Test production

Run `now`, then open the resulting `/asdf` route. The expected error page should render, and logs should include the same message as in development:

```
START RequestId: [id] Version: $LATEST
2019-09-30T20:00:07.799Z	[id]	INFO	Error rendered: 404; Url: /asdf; IP: 8.8.8.8
END RequestId: [id]
REPORT RequestId: [id]	Duration: 26.88 ms	Billed Duration: 100 ms	Memory Size: 3008 MB	Max Memory Used: 87 MB	Init Duration: 241.68 ms
```
