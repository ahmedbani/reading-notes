# Espresso


## Espresso Testing:

Use Espresso to write concise, beautiful, and reliable Android UI tests.

The following code snippet shows an example of an Espresso test:

``` java
        @Test
        public void greeterSaysHello() {
            onView(withId(R.id.name_field)).perform(typeText("Ahmed"));
            onView(withId(R.id.greet_button)).perform(click());
            onView(withText("Hello Ahmed!")).check(matches(isDisplayed()));
        }
```

### Synchronization capabilities

Each time your test invokes onView(), Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:

- The message queue is empty.
- There are no instances of AsyncTask currently executing a task.
- All developer-defined idling resources are idle.

### Synchronization capabilities

The main components of Espresso include the following:

- Espresso – Entry point to interactions with views (via onView() and onData()). Also exposes APIs that are not necessarily tied to any view, such as pressBack().
- ViewMatchers – A collection of objects that implement the Matcher<? super View> interface. You can pass one or more of these to the onView() method to locate a view within the current view hierarchy.
- ViewActions – A collection of ViewAction objects that can be passed to the ViewInteraction.perform() method, such as click().
- ViewAssertions – A collection of ViewAssertion objects that can be passed the ViewInteraction.check() method. Most of the time, you will use the matches assertion, which uses a View matcher to assert the state of the currently selected view.


## Ridiculous superpower: the Espresso Test Recorder

The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code. By recording a test scenario, you can record your interactions with a device and add assertions to verify UI elements in particular snapshots of your app. Espresso Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.

### Record UI interactions

To start recording a test with Espresso Test Recorder, proceed as follows:
- Click Run > Record Espresso Test.
- In the Select Deployment Target window, choose the device on which you want to record the test. If necessary, create a new Android Virtual Device. Click OK.
- Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it. The Record Your Test window appears after the app launches, and since you have not interacted with the device yet, the main panel reads "No events recorded yet." Interact with your device to start logging events such as "tap" and "type" actions.


### Add assertions to verify UI elements
Assertions verify the existence or contents of a View element through three main types:

- text is: Checks the text content of the selected View element.
- exists: Checks that the View element is present in the current View hierarchy visible on the screen.
- does not exist: Checks that the View element is not present in the current View hierarchy.


**resources:** 

*[https://developer.android.com/training/testing/espresso](https://developer.android.com/training/testing/espresso)*

*[https://developer.android.com/studio/test/espresso-test-recorder](https://developer.android.com/studio/test/espresso-test-recorder)*


