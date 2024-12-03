# Cub3D: A simple C-based raycasting game

This **Cub3D** project is my 10th project at Codam. The project is based on creating a Wolfenstein-like 3D raycasting algorithm, making a 2D map look like you are in a 3D world. This project was a team project but easily separated into two parts: parsing of the map & rendering of the game, which made it feel more like a solo project. I built the rendering part of the game. The algorithm to calculate the distance to a wall and then the height of the wall was the most challenging part.

The code can be found on my project partners github:
[Cub3D code](https://github.com/kennyohhst/cub3d)

## Project Highlights

- **Raycasting algorithm**: Writing a custom distance calculating algorithm was super interesting and infuriating to do, but cool nonetheless!
- **Game loop**: Writing a smooth game loop that reads input well was essential for a smooth user experience.
- **Efficient pixel placing**: I spent a lot of time optimizing the placing of pixels. I used to first place the background and then render the walls over it but later changed to only using one image and place each pixel only once to get better performance.

## The Project

The **Cub3D** project is split up into rendering and parsing.

- **Core Functionality**: Cub3D takes a map that contains the pixel and map data and uses it to generate the game.
- **Parsing**: My project partner handled the parsing. It involved reading the map and storing it, checking that the player is surrounded by walls, and making sure there was no missing data.
- **Rendering**: The rendering part involved calculating the distance to the closest wall each game loop. A fast calculation and a fast pixel placing algorithm created the best game experience. The shorter the time to calculate these values, the higher the FPS reached by the game.
- **Moving**: Player movement was also interesting as the key input generates a different direction based on the way the player is viewing. I used cos() and sin() to calculate the direction.
- **Standards**: I used defines in the header to set things like movement speed, FOV, and window size. This way, these variables could easily be changed, and the program would still function well.

### Challenges

Developing **Cub3D** had two big challenges:

- Understanding how to use a radian for direction and knowing what way the player is facing based on cos() and sin() involved learning about and understanding some mathematics.
- The distance calculating algorithm was something that took me quite a while. If it is slightly wrong, you get very hard to interpret output, and fixing it seemed impossible. After two weeks of struggling, I decided to rewrite the entire thing and got it right almost immediately in one day.

### How to Run

To run the **Cub3D** program:

```bash
make run
```

For a custom map or after changing MS variables in the header you can try:

```bash
make
./cub3d /maps/custommap.cub
```

## Conclusion

The **Cub3D** project was a mathematical challenge that encouraged me to understand the underlying algorithms well and pushed me to code optimization, as I could visibly see the program run better with every improvement. It was overall very fun to have this end-result after some weeks of hard work.