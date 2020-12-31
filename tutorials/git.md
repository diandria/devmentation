# GIT
## Shortcuts
- No terminal
Para abrir no Visual Code
`$ git config --global core.editor code`

	Para abrir no VIM
`$ git config --global --editor`

- Na IDE:
```
[user]
	email = your_name@mail.com
	name = Your Name
[core]
	editor = code
[alias]
	s = !git status -s
	c = !git add --all && git commit -m
	l = !git log --pretty=format:\"%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr\"
```