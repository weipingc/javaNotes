# JVM arguments
```
It varies on implementation and version, but usually it depends on the VM used (e.g. client or server, see -client and -server parameters) and on your system memory.

Often its default value is 1/4th of your physical memory or 1GB (whichever is smaller).

Also Java configuration options (command line parameters) can be "outsourced" to environment variables including the -Xmx, which can change the default (meaning specify a new default). Specifically the JAVA_TOOL_OPTIONS environment variable is checked by all Java tools and used if exists (more details here and here).

You can run the following command to see default values:

java -XX:+PrintFlagsFinal -version

It gives you a loooong list, -Xmx is in MaxHeapSize, -Xms is in InitialHeapSize.
```
