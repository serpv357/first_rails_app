# README

Ruby Version: 2.7.6

Uses postgresql. Ensure postgres installed.

Some of the below instructions are for MacOS and may have to be modified for Windows.

If not already there, create a new database role for the application with 'createuser -P -d {name_of_your_application}'

Put the password in your .zprofile or .bash_profile with a line like this: export {your_app_name}_DATABASE_PASSWORD="{password_from_previous_step}"

Edit the database.yml file, modifying the default so that it includes
  username: {your_app_name}
  password: <% ENV['{your_app_name}_DATABASE_PASSWORD'] %>

Run 'rails db:create' in path of application

Run 'bin/rails server' to start the server
