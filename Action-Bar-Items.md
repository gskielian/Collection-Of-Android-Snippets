# Action Bar Items

(some cool icons to use with this [here](https://google.github.io/material-design-icons/))

There is a 2.5 step process for adding action bar items:

### 1) locate the onCreateOptionsMenu method and open the xml-file
This will be in the res/menu folder.

In the example below, the name of the xml file is menu_main.xml:

```java
    public boolean onCreateOptionsMenu(Menu menu) {
        // Inflate the menu; this adds items to the action bar if it is present.
        getMenuInflater().inflate(R.menu.menu_main, menu);
        return true;
    }
```

### 2) add an item in to the menu xml file:

the `id` will be used in step 2.5 (to adjust whether the menu items can become action bar icons, 
change the `app:showAsAction=never` to either "ifRoom" "always" or "never"
(the catch is that you will need to give it an icon (i.e. add a line `android:icon="@drawable/abc_ic_search_api_mtrl_alpha"`)


```xml
<menu xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    tools:context="io.spectruminnovations.www.urbonfood_v01.MainActivity">
    <item android:id="@+id/action_settings"
        android:title="@string/action_settings"
        app:showAsAction="never" />
</menu>
```

### 2.5) have the button do something when pressed -- this is the easy part (hence the 0.5)



```java
    public boolean onOptionsItemSelected(MenuItem item) {
        int id = item.getItemId();

        //noinspection SimplifiableIfStatement
        if (id == R.id.action_settings) {
        //place stuff to do here with when the item of said id is pressed

        return true;
        }
        
        return super.onOptionsItemSelected(item);
    }
}
```
