# Pydio Cells docker setup

# Setup

You need create a `.env` file with se follow content:

    # Adapt below values to your local setup

    PUBLIC_FQDN=example.com
    ADMIN_EMAIL=example@gmail.com
    CELLS_ADMIN_PWD=admin

    STORAGE_PATH=/home/myuser/store

    MYSQL_USER=pydio
    MYSQL_DATABASE=cells
    MYSQL_ROOT_PWD=password
    MYSQL_PYDIO_PWD=password

Start the containers:

    $ docker-compose up -d

If you modify the docker-compose.yaml and want to update a service container, you can run:

    $ docker-compose up -d --no-deps --build <name_of_service>

[MIT License](LICENSE)
