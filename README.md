[![](https://jitpack.io/v/CameronPugh/CircleImageView.svg)](https://jitpack.io/#CameronPugh/CircleImageView)

# Circle Image View

A dynamic circular image which can be set via a provided url for Android Applications

## Installation

Add Dependencies to build.gradle.

```bash
dependencies {
    ...
    implementation 'com.github.CameronPugh:CircleImageView:v1.0.1'
   
}
```

## Usage

AndroidManifest.xml
```xml
    <uses-permission android:name="android.permission.INTERNET" />
```
your_activity.xml
```xml
    <com.circleimageview.CircleImageView
        android:id="@+id/image"
        android:layout_width="100dp"
        android:layout_height="100dp"
        android:layout_gravity="center">
    </com.circleimageview.CircleImageView>
```
your_activity.java
```java
   private ImageRequester imageRequester;
   ...
   imageRequester = ImageRequester.getInstance(getApplicationContext());
   ...
   String url = "https://static.wikia.nocookie.net/marvelcinematicuniverse/images/b/b2/Doctor_Strange_MoM_Profile.jpeg/revision/latest?cb=20211229010907";

   CircleImageView image = findViewById(R.id.image);
   imageRequester.setImageFromUrl(image, url);

```

## Source
This is a class made from Volleys Networked class and hdodenhof CircleImage view. I simply merged the two to create a single image class with both functions. 

See https://github.com/hdodenhof/CircleImageView 

and

https://google.github.io/volley/

for information and credit

## License
[MIT](https://choosealicense.com/licenses/mit/)
 
