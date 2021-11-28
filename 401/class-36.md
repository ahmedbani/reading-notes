
### **Cognito**
#### ***Cognito Installation:***

+ ***Configure Auth Category***

        amplify add auth

        amplify push
     

+ ***Install Amplify Libraries***

        dependencies {
            implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
        }


+ ***Initialize Amplify Auth***

        Amplify.addPlugin(new AWSCognitoAuthPlugin());
        Amplify.configure(getApplicationContext());


+ ***Check the current auth session***

        Amplify.Auth.fetchAuthSession(
            result -> Log.i("AmplifyQuickstart", result.toString()),
            error -> Log.e("AmplifyQuickstart", error.toString())
        );



+ **resources:** 

*[https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/#prerequisites](https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/#prerequisites)*


