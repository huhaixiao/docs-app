# java

```shell
brew tap mdogan/zulu
brew install zulu-sdk17

# Check your other versions of Java
/usr/libexec/java_home -V

# setup Java with zsh
export JAVA_HOME=$(/usr/libexec/java_home -v17.0.10)

java --version
```
