# Installing & Using Postgres
## Learning Goals
- Install Postgres w/ `brew`
- Learn how to interact with Postgres on the command line
- Jot down a few notes on setting up a Rails app to use postgres
- Learn a few command line tricks for Postgres

## Installing Postgres
Let's use `brew` to install postgres:

```bash
$ brew update
$ brew install postgres
```

After `brew` finishes, you'll be given some commands to copypasta into the terminal. These commands are specific to your computer and will set up Postgres to launch on startup. Take a moment to run the commands so we don't have to remember to start Postgres when our computer reboots.

### Trust, but verify
Let's make sure we've got everything we need:

```bash
$ which psql
/usr/local/bin/psql
$ psql -l
```

## Using `psql`
`psql` is the command line interface for Postgres. We can use it to run commands to modify databases or to start a SQL REPL to interact with a database. The `-l` flag tells `psql` to list all the databases on your system. You should have at least one and it's probably got your name. Here are some other super handy CLI options for `psql`:

- `psql -?`: shows all the CLI options w/ descriptions
- `psql -d db_name`: connects to `db_name` and opens a SQL console
- `psql -f path/to/file`: execute all commands in the specified file and then exit
- `psql -l`: show a list of databases and their owners

## Connecting Rails with Postgres


