require 'rubygems'
require 'json'

task :install do
  `apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10`

  `echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.0 multiverse" > /etc/apt/sources.list.d/mongodb-org-3.0.list`
  `apt-get update`
  `apt-get install -y mongodb-org`

  `printf "\\n" |pecl install mongo`

  `echo "extension=mongo.so" > /etc/php5/mods-available/mongo.ini`

  `php5enmod mongo`

  `service apache2 restart`
end
