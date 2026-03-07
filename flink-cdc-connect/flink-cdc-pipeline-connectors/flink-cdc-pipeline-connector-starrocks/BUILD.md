# Building flink-cdc-pipeline-connector-starrocks

Artifact name follows the same pattern as flink-cdc-dist: `flink-cdc-pipeline-connector-starrocks-<revision>-<flink.major.version>.jar`.

## Flink 1.20

```bash
mvn clean install -Dmaven.test.skip=true -Drat.skip=true \
  -pl "flink-cdc-common,flink-cdc-runtime,flink-cdc-flink-compat/flink-cdc-flink-compat-api,flink-cdc-flink-compat/flink-cdc-flink-compat-flink1,flink-cdc-composer,flink-cdc-connect/flink-cdc-pipeline-connectors/flink-cdc-pipeline-connector-starrocks"
```

Output: `target/flink-cdc-pipeline-connector-starrocks-3.6-SNAPSHOT-1.20.jar`

## Flink 2.2

Requires **Java 17**. Set `JAVA_HOME` if needed, e.g. `export JAVA_HOME=$(/usr/libexec/java_home -v 17)`.

```bash
mvn clean install -Pflink-2.2 -Dmaven.test.skip=true -Drat.skip=true \
  -pl "flink-cdc-common,flink-cdc-runtime,flink-cdc-flink-compat/flink-cdc-flink-compat-api,flink-cdc-flink-compat/flink-cdc-flink-compat-flink2,flink-cdc-composer,flink-cdc-connect/flink-cdc-pipeline-connectors/flink-cdc-pipeline-connector-starrocks"
```

Output: `target/flink-cdc-pipeline-connector-starrocks-3.6-SNAPSHOT-2.2.jar`
