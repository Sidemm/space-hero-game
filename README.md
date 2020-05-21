# Space-Hero
A game I designed together with Ali Özkaya for my Senior Design Project.

We created a desktop game application named Space Hero which uses image
recognition to take hand gestures as input. Gesture recognition is achieved by doing calculations on
the image information taken from a webcam in OpenCV. A Unity script imports these OpenCV
methods from the plugin and runs them in the hand recognition script. The user’s hand color is
sampled to segment it from the background, and 10 filters are created with these samples. The
user’s number gestures up to five can be recognized by mainly calculating and counting the cavities
between fingers, this information is used in the spaceship selection menu. The hand is also tracked,
and the tracking point’s location in relation to the middle of the camera screen is used to create the
movement vector of the spaceship. The space contains a constant stream of asteroids and orbs
which are spawned as the player moves forward. The player loses health when they collide with a
asteroid, and an explosion animation plays while the ship is pushed away from the impact location.
Collecting orbs increases the score of the player, which is the main goal of the game.

The game runs with around 60 frames per second, which is satisfactory. We used low
resolutions in hand recognition to increase the execution speed of the hand detection system,
because it has to offer real time tracking and gesture recognition. Overall if the segmentation
process is successful the program works as desired, but the user’s surrounding can greatly reduce
the accuracy of segmentation. This result was expected because we only use a webcam for hand
recognition instead of more accurate tools like Leap or Kinect. We did not want to develop our
program using these tools because we wanted to write our own segmentation algorithm and we
wanted our application to be more accessible as these tools are rare.



