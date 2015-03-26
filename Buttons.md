# Buttons
CopyPasta for different button types

## Button
```
Button bob = (Button) findViewById(R.id.button);

bob.setOnClickListener(new View.OnClickListener() {
  public void onClick(View view) {
      // write something to do if clicked below
    
  }
  
});
```

## ToggleButton
```java
ToggleButton rufus = (ToggleButton) findViewById(R.id.toggleButton);

rufus.setOnClickListener(new View.OnClickListener() {
  public void onClick(View view) {
      // am I checked?
      boolean on = ((ToggleButton) view).isChecked();
      
      if (on) {
          // write something to do if checked below
          
      } else {
          // write something to do if not checked below
          
      }
  }
});
```
