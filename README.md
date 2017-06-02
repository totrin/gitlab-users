# gitlab-users

A simple command line interface to handle GitLab user accounts, based on [python-gitlab](https://github.com/python-gitlab/python-gitlab).

## Installation

- Install the package on your system

```
python setup.py install
```

- Edit the `~/.python-gitlab.cfg` following the [python-gitlab package instructions](http://python-gitlab.readthedocs.io/en/stable/cli.html) to setup the GitLab instance to connect with (present version only targets default instance).


## Usage

- Get help

```
gitlab-users -h
```

- List all users with their email

```
gitlab-users
```

- List emails from a given group

```
gitlab-users -g a_group --email-only
```

- Create a list of users from a csv file

```
gitlab-users --create-from example.csv
```

where `example.csv` contains

```
# username, name, email, [organization], [location], [group], [access_level]
wayne,Bruce Wayne,bruce.wayne@wayne-entreprises.com,Wayne Entreprises,Gotham City,Board,owner
kent,Clark Kent,clark.kent@krypton.univ,,Smallville,,
```

- List unused accounts (never sign-in or last connection is older than 1 year)

```
gitlab-users --unused
```

