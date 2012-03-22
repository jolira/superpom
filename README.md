jolira superPOM [![Build Status](https://secure.travis-ci.org/jolira/superpom.png?branch=master)](http://travis-ci.org/jolira/superpom)
=====================================================================================================================

This superpom conveniently adds all our favorite tool to any maven build. It also incorporates all the tools one needs
to upload packages to the Sonatype's OSS, which is the most convienient way we know to get jars into [Maven
Central](http://search.maven.org/#search%7Cga%7C1%7Cjolira).

Please find more information about how to work with Sonatype' OSS at https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide.

In order to be able to upload to sonatype, one has make sure the jars a signed. Details about working with GPG can be
found at http://www.sonatype.com/people/2010/01/how-to-generate-pgp-signatures-with-maven/

The command to release the jars to OSS is:

```
mvn release:prepare release:perform \
      -DperformRelease=true \
      -Dgpg.passphrase=password
```

As discussed in the OSS User Guide, it is essential to have the right credentials at ``˜/.m2/sessings.xml``:

```
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                      http://maven.apache.org/xsd/settings-1.0.0.xsd">
  <servers>
    <server>
      <id>sonatype-nexus-snapshots</id>
      <username>your-jira-id</username>
      <password>your-jira-pwd</password>
    </server>
    <server>
      <id>sonatype-nexus-staging</id>
      <username>your-jira-id</username>
      <password>your-jira-pwd</password>
    </server>
  </servers>
</settings>
```
