You can use this repository as a maven repo in your gradle build. Example of working `build.gradle`:

{% highlight groovy %}

buildscript {
    repositories {
        mavenCentral()
    }

    dependencies {
        classpath 'com.android.tools.build:gradle:PUT_SPECFIC_VERSION_HERE+'
    }
}

repositories {
    mavenCentral()
    mavenLocal()
    maven {
        url "http://bright.github.io/maven-repo/"
    }
}

apply plugin: 'android'
dependencies {
    compile 'com.facebook:facebook-android-sdk:3.19@aar'
    //your other dependencies
}

android {
  //android build setup
}

{% endhighlight %}
