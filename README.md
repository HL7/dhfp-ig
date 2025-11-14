For issues: https://github.com/HL7/dhfp-ig/issues/ or https://github.com/orgs/HL7/projects/8

## CI-Build

* [HL7 FHIR CI Build](https://build.fhir.org/ig/HL7/dhfp-ig/) 
* [Auto-IG build dashboard](https://fhir.github.io/auto-ig-builder/)

## Running the scipt and IG publisher

### Convert script

Convert current computable version of the FM (MAX file) to FHIR IG artifacts.
```
> docker run --name=dhfp-ig -it -v "$(pwd)":/app node:latest /bin/bash
@> (once) wget -O jdk.deb "https://download.oracle.com/java/25/latest/jdk-25_linux-x64_bin.deb" && \
    apt-get update && \
    apt-get install -y ./jdk.deb && \
    rm jdk.deb && rm -rf /var/lib/apt/lists/*
@> (once) apt update; apt install graphviz jekyll
@> (once) git config --global --add safe.directory /app
@> cd script
@> (once) npm install
@> node max2fhir.js
```
Copy grouping & resource json from output.txt into ehrs-ig.json

### Validate

```
(optional) @> curl -L https://github.com/hapifhir/org.hl7.fhir.core/releases/latest/download/validator_cli.jar -o input-cache/validator_cli.jar
@> java -jar validator_cli.jar -version current input/resources -ig input/resources
```

### To build IG

```
(optional) @> curl -L https://github.com/HL7/fhir-ig-publisher/releases/latest/download/publisher.jar -o input-cache/publisher.jar
@> java -jar input-cache/publisher.jar -ig ig.ini
```