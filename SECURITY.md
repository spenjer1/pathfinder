# Reporting a Vulnerability

The steps that are suggested to follow for a step-by-step guide for Pathfinder have a security vulnerability outlined below.
Tthe /app directory is available to public.
This means that anybody who looks at the repo directory to see what to look for can download any file associated with Pathfinder, including the enviornment.ini file.
The /app path needs to be disabled using the steps below.

cd /etc/nginx/sites-enabled
sudo nano pathfinder.conf
Below the section `# Protct /setup with password`, add the following lines of code
```
  # Block /app
  location /app {
   return 403;
```
