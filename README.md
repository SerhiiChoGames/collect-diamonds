# Collect Diamonds

Open source pixel game written with Phaser JS where you need to collect diamonds and avoid the enemy catching you.

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

The Textwire project is licensed under the [MIT License](https://github.com/SerhiiChoGames/collect-diamonds/blob/main/LICENSE)