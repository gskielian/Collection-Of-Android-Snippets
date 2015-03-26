# Timestamps

Sometimes you want timestamps for sensors, events, etc. 

Below are some snippets for different scenarios you would want 

## Precise Time (in seconds since Jan 1st, 1970)

For precise absolute time measurements you should use `System.currentTimeMillis()`.

```Java 
System.currentTimeMillis();
```

## Precise Relative Time Measurements

For precise relative time measurements you should use `System.nanoTime()`.

```Java 
System.nanoTime();
```
