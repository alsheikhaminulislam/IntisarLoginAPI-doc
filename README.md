> Step 1. Add Library 
```
dependencies {
   implementation fileTree(dir: 'libs', include: ['*.jar'])
    ......
  implementation files("libs/firebasemessaging-1.0.0.aar")
```
```
	implementation files("libs/firebasemessaging-1.0.0.aar")
```

> Step 2. Add  XML
```
    <com.alsheikhaminulislam.intisarsignin.IntisarSignin
        android:id="@+id/intisarSignin"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:lntisarButtonBackgroundColor="@color/xxxxxxx"
        app:lntisarSplashImage="@drawable/email_icon"
        />
```


```
    private IntisarSignin intisarSignin; = findViewById(R.id.intisarSignin);
```
```        
    intisarSignin.activeSplashScreen(true,R.drawable.oip);
    intisarSignin.activeSigninAccount(true);
    intisarSignin.activeCreateAccount(true);
    intisarSignin.activeResetPassword(true);
    intisarSignin.activecheckEmailInstructions(true);
    intisarSignin.activecheckEmail(true);

    intisarSignin.activeToolbar(true);


    intisarSignin.setSignupUserEditTextError()
    intisarSignin.setSignupPasswordEditTextError()
    intisarSignin.setSignupConfirmPasswordEditTextError()
    intisarSignin.setCreateNwePasswordEditTextError()
    intisarSignin.setCreateNweConfirmPasswordEditTextError()
    intisarSignin.setResetPasswordEditTextError()
    intisarSignin.setSigninUserEditTextError()
    intisarSignin.setSigninPasswordEditTextError()
```
```
    intisarSignin.setValueEventListener(new ValueEventListener() {
            @Override
            public void onSignInButtonClick(String userID, String password) {

            }

            @Override
            public void onSignupButtonClick(String userID, String password, String confirm_password) {

            }

            @Override
            public void onResetPasswordButtonClick(String password, String confirm_password) {

            }

            @Override
            public void onMailSpikeButtonClick() {
            }

            @Override
            public void onAnotheremailaddressButtonClick() {

            }

            @Override
            public void onMailInstructionsButtonClick(String email) {

            }
            @Override
            public void onBackPressed() {

            }

            @Override
            public void onActivityBackPressed() {

            }
        });
```
```
    @Override
    public void onBackPressed() {
        intisarSignin.onBackPressed();
    }
```


```
        IntisarProgressView intisarProgressView = new IntisarProgressView(this);
```
```
        intisarProgressView.show(R.drawable.email_icon);
        intisarProgressView.setCanceledOnTouchOutside(false);
        intisarProgressView.setBorderW(5);
        intisarProgressView.setBorderColor(R.color.xxxxxxx);
        intisarProgressView.setProgress(60);
        intisarProgressView.setElev(5);
        intisarProgressView.setAutoProgress(10, 10);
```







