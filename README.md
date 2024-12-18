# panel
Infinity is a simple to use Game server management panel

> [!CAUTION]
> Infinity is still in development for a, please wait an release version

## Installation

1. Clone the repository:
   ```bash
   cd /var/www/
   git clone https://github.com/Infinity-Developement/Infinity-Panel.git
   cd panel
   ```

2. Set 755 permissions on the panel directory:
   ```bash
   sudo chown -R www-data:www-data /var/www/Infinity-Panel
   sudo chmod -R 755 /var/www/Infinity-Panel
   ```

3. Install dependencies:
   ```bash
    npm install -g typescript
    npm install --production
   ```

4. Configure the Prisma database and run migrations:
   ```bash
   npm run migrate-deploy
   ```

5. Build the application:
   ```bash
   npm run build-ts
   ```

6. Run the application:
   ```bash
   npm run start
   ```

## Running with pm2 (Optional)

1. Install pm2:
   ```bash
   npm install pm2 -g
   ```

2. Start the application using pm2:
   ```bash
   pm2 start dist/app.js --name "infinity"
   ```

3. Set up pm2 to auto-start on server reboot:
   ```bash
   pm2 save
   pm2 startup
   ```
