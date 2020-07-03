# magento-docker-compose

## Installation Guide
1. Clone the magento-docker-compose repository by executing the following command in the working directory:
`git clone https://github.com/mowadigital/magento-docker-compose.git <name folder>`

2. Go into the folder
`cd <name folder>`

3. Edit the docker-copmose.yml file (with VIM) [VIM cheat Sheet](https://vim.rtorr.com/)
`vi docker-compose.yml`

4. Start editing in VIM press 'i'

5. Replace 'magento002' with magentodemo
*:%s/old/new/g* (replace all old with new throughout file)
`:%s/magento002/magentodemo/g`

6. Save and quit VIM
`:wq`

7. Run Docker (this will create/pull the images)
`docker-compose up -d`

8. View the current containers
`docker ps`

## Setup Magento
- Go to the browser and type the following:
`localhost:8002/setup`

- Click on the 'Agree and Setup Magento' button

### Magento Setup Wizard
1. Click on the 'Start Readiness Check' button
This will check your PHP version, settings, extensions and file permissions

click 'next'

2. Add a database
Database Server Host      -> db
Database Server Username  -> root
Database Server Password  -> root
Database Name             -> magentodemo
Table prefix (optional)   -> leave empty

click 'next'

3. Web cofig
Your Store Address        -> http://localhost:8002/ (already predefined)
Magento Admin Address     -> http://localhost:8002/ <admin link> (also predefined)

4. Customize your store
Store Default Time Zone   -> <choose your timezone>
Store Default Currency    -> <choose your currency>
Store Default Language    -> <choose your default language>
  
5. Create admin account   
New Username              -> <choose a username>
New Email                 -> <fill in an emailaddress>
New Password              -> <choose a password>
Confirm Password          -> <confirm the password>
  
6. READY! 
Click on the 'Install Now' button
