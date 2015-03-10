# Delayed Actions and Simple Threading

Threading is essential in Android, otherwise your UI will be less responsive (temporally).  

If your app's UI is unresponsive for long, an Android device will actually just close your app for the user.

On the other hand, you actually gain some interesting timing abilities with threading utils, making them useful
for single delays and periodic actions (as demonstrated below). 

## One-Time-Delay-Action

```java
final Handler handler = new Handler();
handler.postDelayed(new Runnable() {
  @Override
  public void run() {
    //run the following lines after 2000 milliseconds (= 2 seconds)
  
  }
}, 2000);
```

## Periodic Action 

```java
final Handler handler = new Handler();
handler.postDelayed(new Runnable() {
  @Override
  public void run() {
    //thing to do every 2000 milliseconds (aka every 2 seconds)
  
    handler.postDelayed(this, 2000);
  }
}, 3000); // never reaches this point, so this number doesn't matter
```
