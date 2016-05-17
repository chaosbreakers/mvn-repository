# mvn-repository
openmg maven repository

## deploy

1. release

```
mvn -DaltDeploymentRepository=release-repo::default::file:../mvn-repository/releases clean deploy
```

2. snapshot

```
mvn -DaltDeploymentRepository=snapshot-repo::default::file:../mvn-repository/snapshots clean deploy
```

or add the code in the pom.xml

```xml
<distributionManagement>
    <repository>
        <id>openmg-release</id>
        <url>https://github.com/openmg/mvn-repository/raw/master/releases</url>
    </repository>
    <snapshotRepository>
        <id>openmg-snapshot</id>
        <url>https://github.com/openmg/mvn-repository/raw/master/snapshots</url>
    </snapshotRepository>
</distributionManagement>
```

## dependency

add the code in the pom.xml

```xml
<repositories>
    <repository>
        <id>openmg-release</id>
        <url>https://github.com/openmg/mvn-repository/raw/master/releases</url>
    </repository>
    <repository>
        <id>openmg-snapshot</id>
        <url>https://github.com/openmg/mvn-repository/raw/master/snapshots</url>
    </repository>
</repositories>
```
