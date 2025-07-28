## Docker Environment for Nuxt Starter Projects
This repo provides a lightweight Docker setup for bootstrapping and running a Nuxt 3 project inside a Node.js container.

⚙️ Base Node.js container with bind-mounted project directory

🛠️ Ready for initializing a Nuxt project with npx nuxi init

🔄 Hot-reloading support via volume mounting

🎯 Simple setup for development and testing Nuxt apps

Once the container is running, you can jump in and scaffold a new Nuxt app:

# docker exec -it nuxt-dev sh

# npx nuxi init .

# npm install

# npm run dev
