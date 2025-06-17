This is a temporary fork of the upstream repository that implements SOL-80176.
for the solace-spring-cloud-stream-binder.

## Building / Deployment

**Note**:
Adjust the version number in

- `solace-spring-cloud-stream-binder/solace-spring-cloud-stream-binder-core/pom.xml`
- `solace-spring-cloud-stream-binder/solace-spring-cloud-stream-binder/pom.xml`

Make sure to keep/add the gebitX suffix.

**Deploy**:
```
export NEXUS_THIRDPARTY_REPOSITORY_URL=https://...
mvn -s [settings.xml] -pl solace-spring-cloud-stream-binder/solace-spring-cloud-stream-binder-core,solace-spring-cloud-stream-binder/solace-spring-cloud-stream-binder deploy -DaltDeploymentRepository=thirdparty::default::$NEXUS_THIRDPARTY_REPOSITORY_URL [-DskipTests]
```
