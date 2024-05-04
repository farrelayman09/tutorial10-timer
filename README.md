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
would print out "Farrel's PC: hey hey!" first, then the ones inside the async function (based on the specified conditions)
because the async function was waiting for the future.

