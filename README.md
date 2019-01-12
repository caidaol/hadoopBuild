Problems running Hadoop on Windows

Hadoop requires native libraries on Windows to work properly -that includes to access the file:// filesystem, where Hadoop uses some Windows APIs to implement posix-like file access permissions.

This is implemented in HADOOP.DLL and WINUTILS.EXE.

In particular, %HADOOP_HOME%\BIN\WINUTILS.EXE must be locatable.

If it is not, Hadoop or an application built on top of Hadoop will fail.

How to fix a missing WINUTILS.EXE
You can fix this problem in two ways

Install a full native windows Hadoop version. The ASF does not currently (September 2015) release such a version; releases are available externally.
Or: get the WINUTILS.EXE binary from a Hadoop redistribution. There is a repository of this for some Hadoop versions on github.

Then

Set the environment variable %HADOOP_HOME% to point to the directory above the BIN dir containing WINUTILS.EXE.

Or: run the Java process with the system property hadoop.home.dir set to the home directory.


