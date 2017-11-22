# Basic Android Widgets

Every component you see on your Android Screen is a component of view be it button, edittext or textview.

In XML, we start each element with '<' followed by name of the View Class. Views like Button, EditText are defined inside OS therefore we dont have to specifically define the class, we can use 'Button', 'EditText' etc. After defining the view type we have to give values to certain tags which are neccessary like its height, width. And we can define more tags as per our need. The values for each tag must be given in double quotes.

There are some tags which are common to each and every view defined in android. These are -

**android:id**

This tag is used to declare an unique id for button. Button can be referenced in Java code using this id like findViewById(R.id.givenId)(It returns reference to the button). Convention id to start with 'btn' so we can easily identify button ids in our java code.

**android:layout_height**

This tag is used to define height of the widget. It can be 'match_parent', 'wrap_content' or custom size.
* match_parent means take the full height of the parent laout.

* wrap_content means that the view wants to be just big enough to enclose its content (plus padding)
* Custom size can be in any unit like sp, dp(density independent pixel), px(pixel). But in android it preffered to use dp as the size is independent of the screen pixel and can remain constant on different screens.

**android:layout_width**

This tag is used to define width of the widget. It can be 'match_parent', 'wrap_content' or custom size.
* match_parent means take the full width of the parent laout.

* wrap_content means that the view wants to be just big enough to enclose its content (plus padding)
* Custom size can be in any unit like sp, dp(density independent pixel), px(pixel). But in android it preffered to use dp as the size is independent of the screen pixel and can remain constant on different screens.

Use cases of above tags will become more cleare when we go through specific examples below.

* **Button**

  A user interface element the user can tap or click to perform an action.

  To display a button in an activity, add a button to the activity's layout XML file:

  ```xml
  <Button
    android:id="@+id/btnSubmit"
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:text="Submit" />
    ```


    **android:text**

    This tag contains the text which needs to be displayed inside the button.
