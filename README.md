**Instructions to Run**

Jupyter lab file can be run as normally. The json file must be in the same directory as the jupyter lab file, otherwise the variable for the json path must be updated.

**My Approach**

To start, data is read from the json file using Python's built in json library. This data is put into a dictionary mapping timestamps to a list of possible y values (currentBpm, batteryLevel, anxietyLevel, or baselineProgress). If there are multiple y values for a single timestamp, an average is taken.

A drop factor is defined to potentially optimize this process. For example, a drop_factor of 3 means that only every third data point is kept. 

A list of x and y values is generated based on user parameters, and graphed using the matplotlib library.

The new dictionary data structure makes the program flexible if the user wants to change what y value is being graphed or what time range filter is being used since the structure does not need to be recreated, only the x and y lists need to be regenerated.
