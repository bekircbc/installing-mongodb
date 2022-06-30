# Installing Mongodb on Ubuntu

## if you have old version..

      mongo

      sudo service mongod stop

      mongo

      sudo apt-get purge mongodb-org*

      sudo rm -r /var/log/mongodb

      sudo rm -r /var/lib/mongodb

## after uninstall old version..

      mongo

      wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | sudo apt-key add -

      sudo apt-get install gnupg

      echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/5.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-5.0.list

      sudo apt-get update

      sudo apt-get install -y mongodb-org

      sudo systemctl start mongod

      sudo systemctl status mongod

      mongo

      mongosh
