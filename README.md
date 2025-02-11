# Introduction

ビルドツールの[Gradle](https://docs.gradle.org/current/userguide/userguide.html)を用いて Spring Boot のセットアップを行う

# Setup

dev ディレクトリに`build.gradle`ファイルを追加する

```build.gradle
plugins {
	id 'java'
	id 'org.springframework.boot' version '3.4.2'
}

apply plugin: 'io.spring.dependency-management'

group = 'com.example'
version = '0.0.1-SNAPSHOT'
sourceCompatibility = '17'

repositories {
	mavenCentral()
}

dependencies {
}
```

依存関係の同期

```bash
gradle dependencies
```

gradle wrapper の使用

```bash
gradle wrapper
```

```bash
./gradlew dependencies
```

# Run

以下のコマンドで起動し、`http://localhost:8080/`にアクセスする

```bash
gradle bootRun
```
