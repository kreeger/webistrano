# Webistrano

Capistrano deployment the easy way.

## About

Webistrano is a Web UI for managing Capistrano deployments. It lets you manage projects and their stages (such as test, production, and staging) with different settings. Those stages can then be deployed with Capistrano through Webistrano.

## Installation

### Configuration

Copy `config/webistrano_config.rb.sample` to `config/webistrano_config.rb` and edit it appropriately. In this configuration file you can set the mail settings of Webistrano.

### Database

Copy `config/database.yml.sample` to `config/database.yml` and edit it to match your desired settings. You'll at least need the production database. The others are optional entries for development and testing.

Then create the database structure with Rake:

```
$ cd webistrano
$ RAILS_ENV=production rake db:migrate
```

### Start Webistrano

```
$ cd webistrano
$ ruby script/server -d -p 3000 -e production
```

Webistrano is then available at http://localhost:3000/

The default user is `admin`, the password is `admin`. Please change the password after the first login.

## Authors

- [Jonathan Weiss](mailto:jw@innerewut.de)
- Forked and updated by [Ben Kreeger](mailto:ben@kree.gr)

## License

Code: BSD, see LICENSE.txt
Images: Right to use in their provided form in Webistrano installations. No other right granted.
