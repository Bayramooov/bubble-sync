# Bubble-sync
[Visit](https://bayramooov.github.io/bubble-sync/) the simple canvas experiment exploring tab synchronization through LocalStorage. Enjoy the synchronized movement of bubbles across tabs. A playful journey into web development skills.

![](https://github.com/Bayramooov/bubble-sync/assets/48291004/27b78e02-ddea-48da-a704-8ca5dfdb2ba1)

### Environment Management

- The project utilizes LocalStorage to save and load the environment state, ensuring data persistence.
- Screen boundaries and tab information are dynamically tracked and updated during runtime.
- The canvas is resized to match the current window dimensions, providing a full-screen interactive experience.

### Documentation

#### Bubble Class

The `Bubble` class is responsible for creating and managing individual bubbles. It includes methods for generating random pleasant colors, handling collisions with screen edges, updating bubble positions, and rendering them on the canvas.

#### `constructor(bubble: Object)`

Initializes a new Bubble instance with specified options.

- Parameters:
  - `bubble.x` (optional): Initial X-coordinate of the bubble's center.
  - `bubble.y` (optional): Initial Y-coordinate of the bubble's center.
  - `bubble.radius` (optional): Initial radius of the bubble.
  - `bubble.speedX` (optional): Speed along the X-axis (change in X-coordinate per frame).
  - `bubble.speedY` (optional): Speed along the Y-axis (change in Y-coordinate per frame).
  - `bubble.color` (optional): Color of the bubble.

#### `static randomColor(): string`

Generates a random pleasant color in hsl format.

#### `handleCollisions(screenBounds: Object): void`

Handles collisions with screen edges.

- Parameters:
  - `screenBounds`: Object containing screen boundaries.

#### `update(env: Object): void`

Updates the bubble's position and handles collisions.

- Parameters:
  - `env`: Object containing screen boundaries and canvas context.

#### `render(ctx: CanvasRenderingContext2D): void`

Renders the bubble on the canvas.

- Parameters:
  - `ctx`: The canvas rendering context.

### Functions

#### `bubbleFactory(): Bubble`

Generates a new Bubble with random speeds and default x, y coordinates.

#### `uniqueString(): string`

Generates a unique string combining timestamp and random characters.

#### `canvasFullScreen(canvas: HTMLCanvasElement): void`

Resizes the canvas element to match the current window dimensions.

- Parameters:
  - `canvas`: The canvas element to resize.

#### `saveEnv(env: Object): void`

Saves the environment state to localStorage after converting Bubble objects to plain data.

- Parameters:
  - `env`: The environment object containing Bubble objects and screen dimensions.

#### `loadEnv(tabId: string): Object`

Loads the environment state from localStorage, initializing defaults if needed.

- Parameters:
  - `tabId`: Unique identifier for the current tab.

#### `clearEnv(): void`

Clears the environment state from localStorage.

#### `logInfo(env: Object): void`

Updates HTML elements with environment data for logging.

- Parameters:
  - `env`: The environment data to display.

#### `stopAnimation(): void`

Stops the Animation.

#### `animate(): void`

Animates the bubbles on the canvas, updating their positions and rendering.
