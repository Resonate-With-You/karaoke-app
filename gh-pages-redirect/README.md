# GitHub Pages Redirect to Public IP

This small site is meant to be published with GitHub Pages and immediately redirect visitors to your public IP (and optional port).

How to use

1. Open `index.html` and replace the placeholder `PUBLIC_IP:PORT` with your public IP and optional port. Example: `203.0.113.5` or `203.0.113.5:8080`.
2. Optionally change the protocol in `index.html` from `http://` to `https://` if your server supports TLS.
3. Create a repository on GitHub named `YOUR_GITHUB_USERNAME.github.io` and push the contents of this folder to the `main` branch.

Important notes

- GitHub Pages serves over HTTPS. Redirecting from an HTTPS page to an HTTP target is allowed but will show an insecure destination in the browser. For a secure experience, enable HTTPS on your target or use a dynamic DNS provider with TLS.
- Make sure your router/firewall forwards the appropriate port and your ISP allows inbound connections.
- If your public IP is dynamic, consider using a dynamic DNS service (DuckDNS, No-IP, etc.).

Deploy script

There's a convenience script `deploy.sh` in this folder which shows the git commands to create a repo locally and push it. You still need to create the remote repository on GitHub or use the web UI to initialize it.

If you'd like, provide your GitHub username and public IP and I can fill the placeholders and show exact commands you can run.
