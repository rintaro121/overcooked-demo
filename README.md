# Overcooked Demo
A web application where humans can play Overcooked with trained AI agents.

## Installation

First, install `node` and `npm`, and ensure that you have set up the [overcooked_ai repository](https://github.com/HumanCompatibleAI/overcooked_ai).
Also, install browserify globally, by calling: 

    $ npm install -g browserify

Clone the repo:

    $ git clone git@github.com:HumanCompatibleAI/overcooked-demo.git
    $ cd overcooked-demo

Install using `npm`:

    overcooked-demo $ npm install

Link to the javascript version of the environment code ([this](https://github.com/HumanCompatibleAI/overcooked_ai/tree/master/overcooked_ai_js)). Linking will warn you about vulnerabilities in `overcooked_ai_js`.

    overcooked-demo $ npm link /path/to/overcooked_ai_js/

(If you installed `overcooked_ai` and `overcooked-demo` in the same directory, then you would run `npm link ../overcooked_ai/overcooked_ai_js/`.)

Then build the code:

    overcooked-demo $ npm run build

At this point the code should be ready to run. Start the server with

    overcooked-demo $ node index.js

at which point you should be able to load the website in any browser by going to [http://localhost:8766](http://localhost:8766). At the root directory, you can play the game against pre-trained agents, or watch these agents play each other. At [http://localhost:8766/replay](http://localhost:8766/replay), you can watch replays of fixed trajectories.

If you intend to develop further, we recommend using `nodemon` to avoid having to manually restart the server after making changes:

    $ npm install -g nodemon

Then run the server with `nodemon index.js`.

### Issues

We have sometimes found the animation to break & behave weirdly (and appeared slowed down). This is usually caused by updates to the overcooked gridoworld code (such as switching branches or updating). Uninstalling both `overcooked_ai_js` and `overcooked-demo` and reinstalling them usually fixes the issue (simply restarting one's computer might help too).
