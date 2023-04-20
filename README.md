# Dockers-Odoo
In this repository will deal with how to create an Odoo container in Fedora.

#Updating fedora repository
sudo dnf upgrade

# Install Docker Engine on Fedora

sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Start Docker

sudo systemctl start docker

# Create Odoo container on port 8069

docker run -v /path/to/config:/etc/odoo -p 8069:8069 --name odoo --link db:db -t odoo

or 

docker run -p 8069:8069 --name odoo --link db:db -t odoo -- --db-filter=odoo_db_.*

#Starts Odoo container

docker start -a odoo


