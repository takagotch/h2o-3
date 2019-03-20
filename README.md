### h2o-3
---
https://github.com/h2oai/h2o-3

```
def h2oBranch = 'master'
def h2oBuildNumber = 'nnnn'
def h2oProjectVersion = "x.y.z.${h2oBuildNumber}"

repositories {
  maven {
    url "http://s3.amazonaws.com/h2o-release/h2o-3/${h2oBranch}/${h2oBuildNumber}/maven/repo/"
  }
}
dependencies {
  compile "ai.h2o:h20-core:${h2oProjectVersion}"
  compile "ai.h2o:h2o-algos:${h2oProjectVersion}"
  compile "ai.h2o:h2o-web:${h2oProjectVersion}"
  compile "ai.h2o:h2o-app:${h2oProjectVersion}"
}


```

```
pip install h2o
install.package("h2o")

./gradlew build -x test
brew install npm
java -jar build/h2o.jar

./gradlew syncSmalldata
./gradlew syncRPackages
./gradlew build

export R_LIBS_USER=${WORKSPACE}/Rlibrary
./gradlew syncSmalldata
./gradlew syncRPackages
./gradlew clean
./gradlew build

javac -version
```

```
pkgs <- c("RCurl", "jsonlite", "statmod", "devtools", "roxygen2", "testthat")
for (pkg in pkgs) {
  if (! (pkg %in% rownames(installed.packages()))) install.packages(pkg)
}
```


