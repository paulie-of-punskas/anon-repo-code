### Git functionality
- [ ] detach HEAD, so github does not see the changes made?
- [ ] pre-commit, pre-push hooks?
- [x] clean/empty all files
- [ ] add note to user what will be anonymized

### main.go
- [x] always push to non GitHub first
  - [x] make a 1 second pause, to make sure that github and non github contents are updated?
- [ ] before pushing to GitHub, update index.ts, main.java ... content to:
```
// The code is available elsewhere. Please see the README.md.
```

- [x] add -version
  - ~~versija kiba turetu but irasyta ./config~~

### README.md
- [x] pridet gif su tuom kas vyksta
- [ ] pateikt informacija apie SSH/HTTPS

### CLI
- [ ] add "exclude" flag - comma separated names of files, that will not be emptied
- [x] use "flag" for building CLI
  - https://yourbasic.org/golang/command-line-arguments/
  - https://gobyexample.com/command-line-flags
- [ ] verbose (toks ispudis, kad per daug Printf yra):
```
2026/03/15 16:29:29 Scraping .config ...
2026/03/15 16:29:29 Found remote
2026/03/15 16:29:29 Found url
2026/03/15 16:29:29 Found remote
2026/03/15 16:29:29 Found url
2026/03/15 16:29:29 Remote URL for GitHub has been found!
2026/03/15 16:29:29 Redacting README.md ...
2026/03/15 16:29:29 Scraping .config ...
2026/03/15 16:29:29 Found remote
2026/03/15 16:29:29 Found url
2026/03/15 16:29:29 Found remote
2026/03/15 16:29:29 Found url
2026/03/15 16:29:31 Deleting update_content_for_github branch and switching to v011/flag_version
```

### Tests
- [ ] mock
- [ ] Await when t.Run() ends and print newline
- [ ] CLI