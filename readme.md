# Project : LLM-Store
This is web base project for hosting api's to llm store submitted by the developer making it a centeralised place to use various bots.

## How to Run
### Development
- `docker-compose -f compose-dev.yaml up --remove-orphans` for dev without rebuilding images
- `docker-compose -f compose-dev.yaml up --build --remove-orphans` for dev with images rebuilt

### Production
##### If ssl certs were already generated
- `sudo DOMAIN_NAME=dineshpabbi.xyz IS_VERIFICATION="no" docker compose -f compose-prod.yaml up --remove-orphans` for dev without rebuilding images
- `sudo DOMAIN_NAME=dineshpabbi.xyz IS_VERIFICATION="no" docker compose -f compose-prod.yaml up --build --remove-orphans` for dev without rebuilding images

##### If ssl certs were never generated
- `sudo DOMAIN_NAME=dineshpabbi.xyz IS_VERIFICATION="yes" docker compose -f compose-prod.yaml up --remove-orphans` for dev without rebuilding images
- `sudo DOMAIN_NAME=dineshpabbi.xyz IS_VERIFICATION="yes" docker compose -f compose-prod.yaml up --build --remove-orphans` for dev without rebuilding images

Followed by
- `sudo DOMAIN_NAME=dineshpabbi.xyz IS_VERIFICATION="no" docker compose -f compose-prod.yaml up --remove-orphans` for dev without rebuilding images
- `sudo DOMAIN_NAME=dineshpabbi.xyz IS_VERIFICATION="no" docker compose -f compose-prod.yaml up --build --remove-orphans` for dev without rebuilding images

##### Explanation 
DOMAIN_NAME env variable tells what domain should nginx accept requests for on server
IS_VERIFICATION env variable is a flag which tells docker-compose pipeline if we are yet to verifiy domain with certbot

## Initiating Part for this project.
1. Install latest docker and create an environment for project "llm-store-env"
2. Pull this repo into the container.
3. Please update the stack here, so that we can setup the docker env accordingly. 
