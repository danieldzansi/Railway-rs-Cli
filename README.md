# railway-rs

Deploy your applications from the CLI — like Railway, but yours.

## Install
```bash
curl -fsSL https://raw.githubusercontent.com/danieldzansi/Railway-rs-Cli/master/install.sh | bash
```

## Usage
```bash
# Login
railway-rs login your@email.com

# Deploy your app
railway-rs deploy ./my-app

# View running apps
railway-rs ps

# View logs
railway-rs logs <container-id>

# Stop an app
railway-rs stop <container-id>
```

## How it works

1. CLI compresses your source code
2. Uploads to the Railway RS API
3. API builds a Docker image using Nixpacks
4. Pushes image to registry
5. Worker server pulls and runs the container
6. Your app is live at a subdomain of danieldzansi.me
