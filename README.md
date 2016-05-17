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
