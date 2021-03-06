# CustomInputPIN
Simple library to randomize number in pinpad.

![alt tag](https://raw.githubusercontent.com/siscofran999/CustomInputPIN/master/image/image.jpg)

## Usage
To make a CustomInputPIN add in your layout XML and add CustomInputPIN library in your project or you can also grab it via Gradle:

Add it in your root build.gradle at the end of repositories:

```gradle
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```

Add the dependency :
```build.gradle(:app)
dependencies {
	compile 'com.github.siscofran999:CustomInputPIN:1.1'
}
```

## Implement
```xml 
<com.example.tsmpc47.custominputpin.CustomInputPIN
    android:id="@+id/custom"
    android:layout_width="match_parent"
    android:layout_height="match_parent" />
```

### JAVA
```Java
customInputPIN = findViewById(R.id.custom);
customInputPIN.limitMax(7).limitMsg("Xory, max limit input 7"); // limit max input pin
customInputPIN.setOnResultListener(new ResultListener() {
    @Override
    public void onButtonOK(String result) {
	Log.i(TAG, "onButtonOK: "+result);
    }
    
    @Override
    public void onButtonCancel() {
	Toast.makeText(TesActivity.this, "this is cancel", Toast.LENGTH_SHORT).show();
    }
});
```
LICENCE
-----

CustomInputPIN by [SiscoFran](https://github.com/siscofran999) is licensed under a [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0).
