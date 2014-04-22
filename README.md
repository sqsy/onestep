NOTE: ubuntu1204 in use here

### install ruby with rbenv

- <http://happycasts.net/episodes/38>

### the rmagick stuff, upyun

- [issue 41](https://github.com/happypeter/onestep/issues/41)
- make sure `config/settings.yml` is copied to the new codebase

### passenger

```
gem install passenger
### things needed for passenger
sudo  apt-get install libcurl4-openssl-dev  apache2-prefork-dev  libapr1-dev  libaprutil1-dev
passenger-install-apache2-module
```

### mysql

```
sudo apt-get install mysql-server
```
edit `database.yml` to set the mysql password there

```
rake db:create RAILS_ENV=production
mysql -uroot -pMYPASSWORD onestep_production<onestep_production.sql
```

### uploads
need to cp public/uploads
