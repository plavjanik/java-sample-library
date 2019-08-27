# Java Sample Library

Sample Java library that is published to Bintray.

## Publising to Maven Local

`./gradlew publishToMavenLocal`

## Publishing to Bintray

You need to provide your credentials to Bintray. You can get it from <https://bintray.com/profile/edit>, section `API Key`.

`BINTRAY_USER=user BINTRAY_API_KEY=apikey ./gradlew uploadBintray`

## Using the library

```gradle
plugins {
    id 'java'
}

repositories {
    mavenLocal()
    jcenter()
    maven {
        url  "https://dl.bintray.com/plavjanik/zowe"
    }
}

dependencies {
    implementation 'net.plavjanik.sample:java-sample-library:0.1.8'
}
```
