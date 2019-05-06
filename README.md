# code-server-compose
A docker-compose bundling of the VSC code server (https://github.com/codercom/code-server) with an Nginx reverse proxy

To run:
1. Create a file .secret/code-passwd
2. Contents of the file should be:
```bash
PASSWORD=your_password_here
```
3. Use certbot (or tool of your choosing) to create certificates.
NB: Currently nginx is hard-coded to use ide.towerfamily.org as a url.
TODO: Make this more generic.

4. Copy `docker-compose.yml.template` to `docker-compose.yml`.

5. Update `#### SET ME ####` references in docker-compose.yml to point to your actual certificate/key file locations.

6. `docker-compose up -d`
