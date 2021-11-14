# Intents, Activities, and SharedPreferences

## Android Tasks and the Back Stack:

### Understand Tasks and Back Stack

To summarize the default behavior for activities and tasks:

+ When Activity A starts Activity B, Activity A is stopped, but the system retains its state (such as scroll position and text entered into forms). If the user presses the Back button while in Activity B, Activity A resumes with its state restored.
+ When the user leaves a task by pressing the Home button, the current activity is stopped and its task goes into the background. The system retains the state of every activity in the task. If the user later resumes the task by selecting the launcher icon that began the task, the task comes to the foreground and resumes the activity at the top of the stack.
+ If the user presses the Back button, the current activity is popped from the stack and destroyed. The previous activity in the stack is resumed. When an activity is destroyed, the system does not retain the activity's state.
+ Activities can be instantiated multiple times, even from other tasks.

### Managing Tasks

*The principal <activity> attributes you can use are:*

+ taskAffinity
+ launchMode
+ allowTaskReparenting
+ clearTaskOnLaunch
+ alwaysRetainTaskState
+ finishOnTaskLaunch

*And the principal intent flags you can use are:*

+ FLAG_ACTIVITY_NEW_TASK
+ FLAG_ACTIVITY_CLEAR_TOP
+ FLAG_ACTIVITY_SINGLE_TOP


### Handling affinities

The affinity comes into play in two circumstances:

+ *When the intent that launches an activity contains the FLAG_ACTIVITY_NEW_TASK flag.*
A new activity is, by default, launched into the task of the activity that called startActivity(). It's pushed onto the same back stack as the caller. However, if the intent passed to startActivity() contains the FLAG_ACTIVITY_NEW_TASK flag, the system looks for a different task to house the new activity. Often, it's a new task. However, it doesn't have to be. If there's already an existing task with the same affinity as the new activity, the activity is launched into that task. If not, it begins a new task.

If this flag causes an activity to begin a new task and the user presses the Home button to leave it, there must be some way for the user to navigate back to the task. Some entities (such as the notification manager) always start activities in an external task, never as part of their own, so they always put FLAG_ACTIVITY_NEW_TASK in the intents they pass to startActivity(). If you have an activity that can be invoked by an external entity that might use this flag, take care that the user has a independent way to get back to the task that's started, such as with a launcher icon (the root activity of the task has a CATEGORY_LAUNCHER intent filter; see the Starting a task section below).

+ *When an activity has its allowTaskReparenting attribute set to "true".*
In this case, the activity can move from the task it starts to the task it has an affinity for, when that task comes to the foreground.

For example, suppose that an activity that reports weather conditions in selected cities is defined as part of a travel app. It has the same affinity as other activities in the same app (the default app affinity) and it allows re-parenting with this attribute. When one of your activities starts the weather reporter activity, it initially belongs to the same task as your activity. However, when the travel app's task comes to the foreground, the weather reporter activity is reassigned to that task and displayed within it.


## Android SharedPreferences:

You can create a new shared preference file or access an existing one by calling one of these methods:

getSharedPreferences() — Use this if you need multiple shared preference files identified by name, which you specify with the first parameter. You can call this from any Context in your app.
getPreferences() — Use this from an Activity if you need to use only one shared preference file for the activity. Because this retrieves a default shared preference file that belongs to the activity, you don't need to supply a name.
For example, the following code accesses the shared preferences file that's identified by the resource string R.string.preference_file_key and opens it using the private mode so the file is accessible by only your app:

        Context context = getActivity();
        SharedPreferences sharedPref = context.getSharedPreferences(
                getString(R.string.preference_file_key), Context.MODE_PRIVATE);



**resources:** 

*[https://developer.android.com/guide/components/activities/tasks-and-back-stack](https://developer.android.com/guide/components/activities/tasks-and-back-stack)*


*[https://developer.android.com/training/data-storage/shared-preferences](https://developer.android.com/training/data-storage/shared-preferences)*

