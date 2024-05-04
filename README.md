# Tutorial 10 Timer
Farrel Ayman Abisatyo  <br>
2206828916 <br>
Advanced Programming B <br>

## Reflection
### 1. Experiment 1.2: Understanding how it works.

<img src= "assets/images/Screen Shot 2024-05-04 at 17.41.39.png" width="600px"> <br>
Observing the output in the terminal, it can be seen that the "Farrel's PC: hey hey!" occurs
before the "Farrel's PC: howdy!" and "Farrel's PC: done!". This is because the code
of the "Farrel's PC: hey hey!" message itself was not inside of the async function. Thus, it 
would print out "Farrel's PC: hey hey!" first, then the ones inside the async function (based on the specified conditions).
This is because the async function was waiting for the result of the future. It can also be observed that the
first and second message are shown at almost the exact same time, while the third was late 2 secs because of the nature
of the async function itself that surrounds the second and third message.

### 2. Experiment 1.3: Multiple Spawn and removing drop

<img src= "assets/images/Screen Shot 2024-05-04 at 18.00.36.png" width="600px"> <br>
After looking at the output, it can be seen that having multiple spawners leads to an 
increased number of tasks because these spawners add more items to the task sender, which functions as a message 
queue. Failing to drop a spawner results in the program not terminating as it still expects further data transmission. 
This can be seen by having only the hovering cursor being visible instead of the usual command prompt consisting of the username,
hostname, and working directory, in this case:

```farrelayman@Farrels-MacBook-Pro timer %```

When a spawner invokes the spawn function, it generates a new task and sends it to 
the task sender. The executor retrieves tasks from the task sender, executing one at a time, then proceeds to the next task 
until there are no more tasks left and the spawner has been dropped, indicating that the interaction has ended.