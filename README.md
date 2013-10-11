Tired of typing

  ../../gradlew build

to execute gradle in a project that uses gradle wrapper?

Use the gradle wrapper wrapper!
The script, located at TNM/trunk/gradle/wrapper/gradle-wrapper-wrapper, checks
if the current directory lies within a subversion or git working copy with
gradle wrapper located at the trunk's root. In that case the call is delegated
to the gradle wrapper, otherwise it is delegated to the gradle binary installed
on your system.

For maximum fidelity, copy the file gradle-wrapper-wrapper into your path
(e.g. /opt/bin, /usr/local/bin, ...) and add an alias into your .bashrc file.

Example:

  cp gradle/wrapper/gradle-wrapper-wrapper ~/bin
  echo "alias gradle=gradle-wrapper-wrapper" >> ~/.bashrc
  source ~/.bashrc
  
From now on you can just type "gradle ..." and the correct gradle binary is
exeucted. Happiness ensues!
