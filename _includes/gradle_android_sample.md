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

apply plugin: 'com.android.application'

dependencies {
    compile '{{ include.groupId }}:{{ include.artifactId }}:{{ include.versions | last}}@aar'
    //your other dependencies
}

android {
  //android build setup
}

{% endhighlight %}
