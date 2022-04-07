# CS568 Workshop - Timer

Impliment https://simpletouchsoftware.com/timers/tabatapro/.

- A workout consists of 10 sets for 5 mins.
- Every set consists of 20 secs workout and 10 secs rest.
- The application will display a "Start" button, once clicked, you will alternate a green background with a decrementing 20 secs timer in the center, followed by a decrementing 10 secs timer with a red background. When a total of 10 sets is finished, reset the app to the initial state.
- During workout, users should be able to "stop" the timer and go back to initial state.
- Style it (Change background colors of the divs).
- Take input for cycles, workout, rest time

Algorithm

```
cycles
phase //idle, workout, rest
totalTime
displayedNum

intervalId = null 

startWorkout
    intervalId = setInterval(tickFunction, 1000);

stopWorkout
    clearInterval(intervalId);
    set the state back to default

tickFunction
	count down cycles
	based on current displayed number and phase, set the next phase and displayed number

Edge case:
  set idle to workout
```
