# Intent Filters:

### ***Allowing Other Apps to Start Your Activity:***
If your app can perform an action that might be useful from another app, your app should be prepared to respond to action requests by specifying the appropriate intent filter in your activity.

#### **Add an Intent Filter**
+ ***Action***
A string naming the action to perform. Usually one of the platform-defined values such as ACTION_SEND or ACTION_VIEW.
Specify this in your intent filter with the <action> element. The value you specify in this element must be the full string name for the action, instead of the API constant (see the examples below).

+ ***Data***
A description of the data associated with the intent.
Specify this in your intent filter with the <data> element. Using one or more attributes in this element, you can specify just the MIME type, just a URI prefix, just a URI scheme, or a combination of these and others that indicate the data type accepted.

+ ***Category***
Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started. There are several different categories supported by the system, but most are rarely used. However, all implicit intents are defined with CATEGORY_DEFAULT by default.
Specify this in your intent filter with the <category> element.


### **Handle the Intent in Your Activity:**
As your activity starts, call getIntent() to retrieve the Intent that started the activity. You can do so at any time during the lifecycle of the activity, but you should generally do so during early callbacks such as onCreate() or onStart().

For example:

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        setContentView(R.layout.main);

        // Get the intent that started this activity
        Intent intent = getIntent();
        Uri data = intent.getData();

        // Figure out what to do based on the intent type
        if (intent.getType().indexOf("image/") != -1) {
            // Handle intents with image data ...
        } else if (intent.getType().equals("text/plain")) {
            // Handle intents with text ...
        }
    }

#### **Return a Result:**
If you want to return a result to the activity that invoked yours, simply call setResult() to specify the result code and result Intent. When your operation is done and the user should return to the original activity, call finish() to close (and destroy) your activity.



+ **resources:** 

    *[https://developer.android.com/training/basics/intents/filters](https://developer.android.com/training/basics/intents/filters)*


