To-Do Web App
=============

This (Yet Another) To-Do web application is written using **Play Framework, Java, Scala and Aerospike.**

The code is easy to follow and substantial enough to be a foundation in learning how to leverage Aerospike's technology in writing modern applications along with other popular technologies. This app may also be used as a "seed" application that you can expand.

### App Features

  * Create To-Dos
  * Batch Read and Display To-Dos
  * Delete To-Dos

### Aerospike Java Client APIs Used

  * **connect** - For establishing connection to the Aerospike Cluster. This is **done once when the app starts.** See custom Play Plugin* [ASPlugin](https://github.com/aerospike/play-scala-java-aerospike-app/blob/master/ASPlugin.java)
  * **get** - For single-record and multiple-records read operations
  * **put** - For write operations
  * **close** - For closing connection to the Aerospike Cluster. This is **done once when the app terminates.** See custom Play Plugin* [ASPlugin](https://github.com/aerospike/play-scala-java-aerospike-app/blob/master/ASPlugin.java)

Note: To learn more about writing Play Plugins, [click here](https://www.playframework.com/documentation/2.3.x/JavaPlugins).

## Get Up and Running

### Prerequisites

- [Aerospike Server](http://www.aerospike.com/download/server/latest) – The server should be running and accessible from this app.
- [Typesafe Activator](http://typesafe.com/platform/getstarted) - It is used to build and run the application.

**Note:** [Aerospike Java Client 3.0.30](https://github.com/aerospike/play-scala-java-aerospike-app/tree/master/lib) comes bundled with this app. If you'd like to use the latest version, [click here](http://www.aerospike.com/download/client/java/latest/) to download it. Then, be sure to replace the jar in */lib* folder.

### Usage

#### Config

In [conf/application.conf](https://github.com/aerospike/play-scala-java-aerospike-app/blob/master/conf/application.conf), update **aerospike.cluster.ip** and **aerospike.cluster.port** under *Aerospike Cluster Configuration* section such that they point to your server running Aerospike Server.

#### Build and Run

To build and run the application, run command **activator run** from application's root folder.

If all is well, open web browser and point it to: [http://localhost:9000](http://localhost:9000).

You should see:

<img src="https://github.com/aerospike/play-scala-java-aerospike-app/blob/master/public/images/app.png"/>

If you see **Oops! Connection to Aerospike cluster failed! Please check your Aerospike IP and Port settings in application.conf**, please make sure your Aerospike Server is running and available to this app. Also confirm that **aerospike.cluster.ip** and **aerospike.cluster.port** are set correctly as described above in the Config section.

### Learn More

To learn more about code snippets from this app, [visit this blog](http://www.iamontheinet.com/2014/10/24/simple-to-do-web-app-using-java-aerospike-play-and-scala/).
