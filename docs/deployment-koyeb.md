# deployment-koyeb    


## [cli](https://www.koyeb.com/docs/build-and-deploy/cli/installation)    

```bash
curl -fsSL https://raw.githubusercontent.com/koyeb/koyeb-cli/master/install.sh | sh
```

`.bashrc` or `.zshrc`
```bash

export PATH=$HOME/.koyeb/bin:$PATH
```


```yml
app:
  # Should be the same as backend.baseUrl when using the `app-backend` plugin
  baseUrl: https://engineering-portal.koyeb.app

backend:
  baseUrl: https://engineering-portal.koyeb.app
  listen:
    # The $PORT environment variable is a feature of Koyeb
    # https://www.koyeb.com/docs/apps/services
    port: ${PORT}

```


```bash
koyeb app init example-backstage \
  --git github.com/<YOUR_GITHUB_USERNAME>/<YOUR_REPOSITORY_NAME> \
  --git-branch main \
  --ports 8000:http \
  --routes /:8000 \
  --env PORT=8000
```
