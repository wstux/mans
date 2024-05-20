# gitconfig

## Simple gitconfig

.gitconfig
```
[user]
	email = <email>
	name = <name>
[core]
	editor = vim
```

Example

.gitconfig
```
[user]
	email = my-mail@email.com
	name = Second_name First_name
[core]
	editor = vim
```

## Gitcondif with auto login

.gitconfig
```
[user]
	email = <email>
	name = <name>
[core]
	editor = vim
[credential "https://<accaunt>/"]
	provider = generic
[credential]
	helper = store
```

.git-credentials
```
https://<user>:<password>@<accaunt>
```

Example

.gitconfig
```
[user]
	email = my-mail@email.com
	name = Second_name First_name
[core]
	editor = vim
[credential "https://github.com/"]
	provider = generic
[credential]
	helper = store
```

.git-credentials
```
https://githubuser:github_token@github.com
```

