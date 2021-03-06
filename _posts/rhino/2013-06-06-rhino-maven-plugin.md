---
layout: post
category : Javascript
tagline: "rhino-maven-plugin 1.0.1 released"
tags : [Maven, Javascript, Mozilla Rhino]
---
*rhino-maven-plugin* is a Maven plugin to compile Javascript to Java class file using Mozilla Rhino. The compiled classes require Mozilla Rhino to run. The plugin is licensed under the Mozilla Public License 2.0 due to MPL being the license for Rhino

Maven Distribution
{% highlight xml %}
<build>
  <plugins>
    <plugin>
      <groupId>de.skiptag</groupId>
      <artifactId>rhino-maven-plugin</artifactId>
      <version>1.0.1</version>
    </plugin>
  </plugins>
</build>
{% endhighlight %}
You can start the compilation be simply calling
  mvn rhino:compile
or by adding the following to the plugin tag:
{% highlight xml %}
<executions>
  <execution>
    <phase>compile</phase>
    <goals>
      <goal>compile</goal>
    </goals>
  </execution>
</executions>
{% endhighlight %}
Mozilla Rhino as dependency
{% highlight xml %}
<dependency>
  <groupId>org.mozilla</groupId>
  <artifactId>rhino</artifactId>
  <version>1.7R4</version>
</dependency>
{% endhighlight %}
The artifact is deployed to Maven Central so no repository configuration should be necessary.
