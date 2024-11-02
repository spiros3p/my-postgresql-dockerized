# my-postgresql-dockerized

- postgreSQL
- pgadmin4

## Tasks

***NS: not started | WIP: in progress***
- (NS) .env file is not used 
- (NS) implement domain with nginx reverse proxy

## Usage

### Connect

- Hit the localhost port that PgAdmin instance is running (default: 8881)
- Use the PGadmin credentials as defined in the compose.yml to log in
- Right click **Servers** > **Register** > **Server...**
- In **General** tab > pick a **Name** for the new connection (anything)
- In **Connection** tab
    - for **Host name/address** use the service name in the compose.yml (default: postgress)
    - for **Port** define the port from the compose.yml file (default: 5432)
    - for **Username** define the port from the compose.yml file (default: user)
    - for **Password** define the port from the compose.yml file (default: pass)

### Create new DB and User

#### New User
- Right click **Login/Group Roles** > **Create** > **Login/Group Role...**
- In **General** tab > provide **Name** for the new user
- In **Definition** tab > provide **password** for the new user
- In **Privileges** tab > adjust privilages for the new user
- Click **Save**

#### New DB
- Right click **Databases** > **Create** > **Database...**
- In **General** tab > provide **Database** name for the new DB
- In **General** tab > provide **Owner** for the new DB (the new user created earlier)
- In **Security** tab > add **privileges** for the new user to have the necessary access
- Click **Save**