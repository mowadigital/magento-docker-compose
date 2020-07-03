# magento-docker-compose

## Installation Guide
1. Clone the magento-docker-compose repository by executing the following command in the working directory:<br />
`git clone https://github.com/mowadigital/magento-docker-compose.git <name folder>`

2. Go into the folder<br />
`cd <name folder>`

3. Edit the docker-copmose.yml file (with VIM) [VIM cheat Sheet](https://vim.rtorr.com/)<br />
`vi docker-compose.yml`

4. Start editing in VIM press 'i'

5. Replace 'magento002' with magentodemo<br />
*:%s/old/new/g* (replace all old with new throughout file)<br />
`:%s/magento002/magentodemo/g`

6. Save and quit VIM<br />
`:wq`

7. Run Docker (this will create/pull the images)<br />
`docker-compose up -d`

8. View the current containers<br />
`docker ps`

## Setup Magento
- Go to the browser and type the following:<br />
`localhost:8002/setup`

- Click on the 'Agree and Setup Magento' button

### Magento Setup Wizard
1. Click on the 'Start Readiness Check' button

This will check your PHP version, settings, extensions and file permissions<br />

click 'next'<br />

2. Add a database

Database Server Host      -> db<br />
Database Server Username  -> root<br />
Database Server Password  -> root<br />
Database Name             -> magentodemo<br />
Table prefix (optional)   -> (leave empty)<br />

click 'next'<br />

3. Web cofig

Your Store Address        -> http://localhost:8002/ (already predefined)<br />
Magento Admin Address     -> http://localhost:8002/(adminlink) (also predefined)<br />
  
click 'next'<br />

4. Customize your store

Store Default Time Zone   -> "choose your timezone"<br />
Store Default Currency    -> "choose your currency"<br />
Store Default Language    -> "choose your default language"<br />
  
click 'next'<br />
  
5. Create admin account

New Username              -> "choose a username"<br />
New Email                 -> "fill in an emailaddress"<br />
New Password              -> "choose a password"<br />
Confirm Password          -> "confirm the password"
  
click 'next'<br />
  
6. READY! 
Click on the 'Install Now' button
