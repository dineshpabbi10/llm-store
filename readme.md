# Project : LLM-Store
This is web base project for hosting api's to llm store submitted by the developer making it a centeralised place to use various bots.

## How to Run
### Development
- `docker-compose -f compose-dev.yaml up --remove-orphans` for dev without rebuilding images
- `docker-compose -f compose-dev.yaml up --build --remove-orphans` for dev with images rebuilt

### Production
- `docker-compose -f compose-prod.yaml up --remove-orphans` for dev without rebuilding images
- `docker-compose -f compose-prod.yaml up --build --remove-orphans` for dev with images rebuilt

## Initiating Part for this project.
1. Install latest docker and create an environment for project "llm-store-env"
2. Pull this repo into the container.
3. Please update the stack here, so that we can setup the docker env accordingly. 
