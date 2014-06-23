# Wrapping the gradle wrapper

Tired of typing
```bash
../../gradlew build
```

to execute gradle in a project that uses gradle wrapper?

*Enter the gradle-wrapper wrapper!*

The script `gradle-wrapper-wrapper` checks if the current directory lies within
a git or subversion working copy with gradle wrapper located at the trunk's root.
In that case the call is delegated to the gradle wrapper, otherwise it is delegated
to the gradle binary installed on your system.

For maximum fidelity, copy the file gradle-wrapper-wrapper into your path
(e.g. `~/bin`, `/opt/bin`, `/usr/local/bin`, ...) and add an alias into your .bashrc file.

Example:

```bash
cp gradle-wrapper-wrapper ~/bin
echo "alias gradle=gradle-wrapper-wrapper" >> ~/.bashrc
source ~/.bashrc
```  

From now on you can just type `gradle ...` from whereever you are  and the correct gradle
binary is exeucted. Happiness ensues!

![Inception!](https://raw.github.com/mattgruter/gradle-wrapper-wrapper/master/inception.png)

