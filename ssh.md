## Setup SSH GitHub

1. Create ssh config:

	```
	# Github: user1
	Host github.com
	   HostName github.com
	   IdentityFile ~/.ssh/user1
	   IdentitiesOnly yes

	# Github: user2
	Host github.user2
	   HostName github.com
	   IdentityFile ~/.ssh/user1
	   IdentitiesOnly yes
	```

3. Generate SSH key pairs:

	`ssh-keygen -t ed25519 -C "user1@gmail.com" -N Password -f .ssh/user1`
	`ssh-keygen -t ed25519 -C "user2@gmail.com" -N Password -f .ssh/user2`

2. Edit .ssh/config file (just copy over)

3. Add ssh keys to system:
	`ssh-add user1`
	`ssh-add user2`

4. Test connection:

	`ssh -T git@github.com`
	`ssh -T git@github.user2`

5. Install git cli: https://github.com/cli/cli

6. gh auth login and choose ssh method to authenticate your git accounts.
