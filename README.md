# NetlifyCMS GitHub OAuth Provider Server

This is the server side. The side that handles the GitHub OAuth handshake.

### 2. Create a GitHub OAuth App

On GitHub, go to Settings > Developer Settings > OAuth apps > New OAuth app. Or use this [direct link](https://github.com/settings/applications/new).

Complete the form using the following values.

**Application name**: Anything you want to call it. This won't effect functionality.

**Homepage URL**: This *must* be the URL to your remix of this Glitch. Go to Show > In a New Window and grab the URL from there. You'll also use this in your NetlifyCMS config.yml

**Application description**: Anything you want. This won't effect functionality.

**Authorization callback URL**: This *must* be the URL to where this app is deployed followed by `/callback`. If you need a path other than `callback`, you can change that in `index.js`.

### 3. Add Your OAuth App's Client ID and Secret to .env

In GitHub, go to the GitHub OAuth App you created in step 2. Locate the Client ID and Client Secret. Set those to the `OAUTH_CLIENT_ID` and `OAUTH_CLIENT_SECRET` in `.evn`

### 4. Configure Your NetlifyCMS client

The one for digital land is in the `content-site` repository in `/admin`

The key item in the client example code and readme is the `base_url` setting in `config.yml`. That's the hook between the client and this server.