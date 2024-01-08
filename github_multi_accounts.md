## Requirements

- Must Have Two Github Accounts.
- Must Have Git Installed.

## Step 1: Generate SSH Keys

Generate **two** ssh keys for two different github account email using the command below

```bash
ssh-keygen -t ed25519 -C "first_email@gmail.com"
ssh-keygen -t ed25519 -C "second_email@gmail.com"
```

and save them in the **'C:\\Users\\username\\.ssh\\'** folder

rename them like this

```bash
id_ed25519_user1
id_ed25519_user1.pub
id_ed25519_user2
id_ed25519_user2.pub
```

## Step 2: Link to Github

Now open your **first** github account made with (first_email@gmail.com) and link the `id_ed25519_user1.pub` with github account's SSH setting.

Then open your **second** github account made with (second_email@gmail.com) and link the `id_ed25519_user2.pub` with github account's SSH setting.

## Step3: Create Config File

Now it's time to create the **config** file in your **'C:\Users\username\.ssh\'** folder

```bash
Host user1 github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile C:\Users\your_username\.ssh\id_ed25519_user1

Host user2 github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile C:\Users\your_username\.ssh\id_ed25519_user2

```

## Step 3: Cloning the repository

Now clone the repository of first project using ssh link from github

```bash
git clone git@github.com:first_username/test.git

#replace 'github.com' with 'user1' as user1's email is linked with 'first_username'. Then it will look something like this

git clone git@user1:first_username/test.git

#now hit Enter

```

Similarly clone the repo of second project using ssh link from github

```bash
git clone git@github.com:second_username/test.git

#replace 'github.com' with 'user2' as user2's email is linked with 'second_username'. Then it will look something like this

git clone git@user2:second_username/test.git

#now hit Enter

```

Now you have setup two projects with two different Github accounts in your system.
