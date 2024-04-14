# Tests on the ServeRest API 
API testing using Postman, node and newman ([ServeRest documentation](https://serverest.dev/))

## Technologies used
- Postman
- node v21.7.3
- newman 6.1.2
- newman-reporter-htmlextra

## Environment settings
1. Install node
```bash
# installs NVM (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
 
# download and install Node.js
nvm install 21.7.3
```
2. Install newman
```bash
npm install -g newman
```
3. Install newman-reporter-htmlextra
```bash
npm install -g newman-reporter-htmlextra
```
## Run the tests
### Through the Postman
- Import the environment and collection
- Run tests manually or automatedly

### Through the newman
- Results in CLI
```bash
newman run serveRest.postman_collection.json -e serveRest_env.postman_environment.json -r cli
```
- Results in CLI and HTML page
```bash
newman run serveRest.postman_collection.json -e serveRest_env.postman_environment.json -r cli,htmlextra
```
### Report
- To access the HTML page, simply access the "newman" folder generated in the root directory
