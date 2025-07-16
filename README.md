# Collect Diamonds
![Collect Diamonds](./src/assets/title.png)

Open source pixel game written with Phaser JS where you need to collect diamonds and avoid the enemy catching you.

> [!WARNING]
> The game is not finished yet, but you can play it [here](https://serhiichogames.github.io/collect-diamonds/)

## Installation
The project is written with Phaser JS and Vite. To run the project locally, follow the steps below:

1. Clone the repository
1. Navigate to the project directory
1. Run `npm install` to install the dependencies
1. Run `npm run dev` to start the development server

## Notes
- `init() -> preload() -> create() -> update()` is the order of execution of the functions in the game loop. All the functions are executed only once except `update()` which is executed in a loop for each frame.
- You can flip the sprite with `flipX` and `flipY` properties on the Sprite object. For example, `sprite.flipX = true` will flip the sprite horizontally.
- You can rotate sprites by calling the `setAngle()` method on the Sprite object. For example, `sprite.setAngle(90)` will rotate the sprite by 90 degrees. It rotates based on the origin position of the sprite. By default, it's in the center of the sprite.

## License
The project is licensed under the [MIT License](https://github.com/SerhiiChoGames/collect-diamonds/blob/master/LICENSE)

## Contribute

### NPM Commands
If you a container engine, do these commands inside of a container.

#### Install Dependencies
```bash
npm i
```

#### Watch File Changes
```bash
npm run dev
```

Navigate to `http://localhost:5173/collect-diamonds/` to see your documentation if you run project locally. For containers, visit `http://localhost:3000/collect-diamonds/`.

### With Container Engine
If you use a container engine like [🦦 Podman](https://podman.io/) or [🐳 Docker](https://app.docker.com/), here are the steps that you can make:

#### Build an Image
To build an image, navigate to the root of the project and run this command for Docker:
```bash
docker compose build
```
For Podman, run this:
```bash
podman-compose build
```

#### Run the Container
To run a container, navigate to the root of the project and run this command for Docker:
```bash
docker compose up -d
```
For Podman, run this:
```bash
podman-compose up -d
```

You can visit `http://localhost:3000/collect-diamonds/` to see the game running in container.

#### Copy `node_modules` Locally
To copy `node_modules` directory from the container to your local machine, run this command for Docker:
```bash
docker cp ago-docs:/app/node_modules .
```
For Podman, run this:
```bash
podman cp ago-docs:/app/node_modules .
```

> [!NOTE]
> `node_modules` is excluded from using volume in [compose.yml](compose.yml) file, that's why you need to copy it manually. It's done to prevent your local modules to be copied to Linux container, since it can create incompatibility issues between operating systems if you don't use Linux.

#### Enter the Container
To enter inside of the container, run this command for Docker:
```bash
docker compose exec app sh
```
For Podman, run this:
```bash
podman-compose exec app sh
```

You'll be able to run NPM commands inside of the container.


#### Remove the Container
Run this for Docker:
```bash
docker compose down
```
For Podman, run this:
```bash
podman-compose down
```
