Maze tutorial - Map settings 
============================

Change the map
--------------

You can define your own map for every exercise, to do so you only need to modify the content of the maze.config.json which is in "YourTask/public/maze.config.json".

The image below shows the content of the maze.config.json.

.. container:: text-center

    .. image:: ../images/img_en/maze/maze_config.JPG

|

This maze.config.json gives the map shown below :

.. container:: text-center

    .. image:: ../images/img_en/maze/maze_config_example.JPG

If you wish to modify the map layout, like creating new paths, adding obstacles and so on, you must change the element **"layout"**. **"layout"** is an array of arrays. Each array will represent a map that the student has to solve in this exercice. The meaning of the numbers found in the array can be found in the element **"squareType"** (that you should not have to modify except if you are adding new types of elements to the maze. We will go over them in more details here :



* **0** is an empty tile (that might be populated randomly with non-interactive decor) where the character can’t go.

* **1** is an open tile where the character can walk.

* **2** is the tile where the character starts the game.

* **3** is the goal to reach to win the game.

* **4** is a tile with an obstacle that will kill the character if it walks on it.

* **5** is a special value used if you want to make the start and goal tile the same one.

If you wish to augment or diminish the character's animation speed, update the **"animationSpeed"** element.

If you wish to change the character orientation at the beginning of the task, update the **"startDirection"** element. The character is currently facing SOUTH, you can put WEST, NORTH or EAST.

Multiple maps
-------------

You can add as many maps as you want in the **"layout"** element, as shown in the image below.

Our two maps will, of course, not be displayed at the same time. They are there to ensure that the student doesn’t hardcode the solution to the map he sees. You can add as many maps as you want, with a minimum of one.

When a student submit his code, the correction will test each map individually (in order). If they all pass, the student succeeded.

.. container:: text-center

    .. image:: ../images/img_en/maze/double_layout.JPG

|

In our example, it will look like this (with only the left map being shown):

.. container:: text-center

    .. image:: ../images/img_en/maze/multiple_maze.JPG


