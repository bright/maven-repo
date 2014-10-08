{% highlight groovy %}
dependencies {
    compile '{{ include.groupId }}:{{ include.artifactId }}:{{ include.versions | last}}@aar'
    //your other dependencies
}
{% endhighlight %}
