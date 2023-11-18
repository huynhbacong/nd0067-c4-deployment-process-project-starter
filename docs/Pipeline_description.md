# Pipeline Description
- build steps:
    1. Install node v16.20.2 
    2. Check out code
    3. Install front-end dependencies: `npm run frontend:install`
    4. Install api dependencies: `npm run api:install`
    5. Run front-end lint: `npm run frontend:lint`
    6. Build front-end: `npm run frontend:build`
    7. Build api: `npm run api:build`

- deploy steps (will run only after manual approval):
    1. Install node v16.20.2 
    2. Install EB CLI `eb/setup`
    3. Install AWS CLI `aws-cli/setup`
    4. Check out code
    5. Deploy app `npm run deploy`
