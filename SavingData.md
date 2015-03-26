# Saving Data

- One way is to use a really convenient key-value store called "Shared Preferences"
- A second way is to store onto a file
- A third way is to create your own SqlLite table (this is more involved).

## Shared Preferences 

1)  Make the following class members of your activity (when you are doing the editing especially)

```java
    private SharedPreferences shared_pref;
    private SharedPreferences.Editor editor;
```

2)  initialize sharedPref with your application's context

Place this in your onCreateMethod (after setting the content view)

**Note: Replace "keyval_name_here" with a name for your key-value storage.**

```java
shared_pref = getApplicationContext().getSharedPreferences(
                "keyval_name_here", Context.MODE_PRIVATE);
```

3) add or edit a key-value pair

```
  editor = shared_pref.edit();
  editor.putString("phone_number", "4445556666");
  editor.commit();
```

Similarly there is a `putInt` method for editor as well.


## Retrieving values from SharedPreferences Keystore


Simply enter the key of the int or String, and store the value appropriately:

**Note: Replace "keyval_name_here" with the name for your key-value storage.**

```java

SharedPreferences shared_pref = getApplicationContext().getSharedPreferences(
"keyval_name_here", Context.MODE_PRIVATE);
String default_val = "no phone number";
String phone_number = shared_pref.getString("phone_number", default_val);
```

If you would like, you can display this via a textview:

```java
TextView text_view = (TextView) findViewById(R.id.text_view);
text_view.setText(phone_number);
```

Tada!

===

## Saving to a File

TODO

## Saving to SQLLite database

TODO
