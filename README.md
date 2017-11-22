# Basic Android Widgets

Every UI element you see on your Android Screen is a component of view Class be it a button, textview etc. So for example a Button you see on your screen is defined in a class Button which extends from a class View.

There are two ways to populate UI elements on the screen.
* Your application can create UI elements (and manipulate their properties) programmatically at Runtime.

* Defining UI elements in XML file. THe name of the tag is same as the name of class of the particular view. The advantage to declaring your UI elements in XML is that it enables you to better separate the presentation of your application from the code that controls its behavior.


In XML, we start each element with '<' followed by name of a class that extends a  View Class. Views like Button, EditText are defined inside OS therefore we dont have to specifically give path to the class, we can use 'Button', 'EditText' etc. After defining the UI element we neccessary have to define some attributes like element's height, width. And we can define some more attributes as per our need. The value for each attributes must be given in double quotes.

Special Views which can have multiple views inside them are known as ViewGroups. These include layout files which contains these UI elements. We will talk about them in a seperate article.

There are some attributes which are common to each and every view defined in android. These are -

**android:id**

This attribute is used to declare an unique id for the particular view. View can be referenced in code using this id like findViewById(R.id.givenId)(It returns reference to the button). It is better to start id value with name of the type of UI element. Example in case of Button we can have id start with 'btn' so we can easily identify button ids in our code.

**android:layout_height**

This tag is used to define height of the widget. It can have three different v 'match_parent', 'wrap_content' or custom size.
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
