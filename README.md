jolira superPOM [<img src="https://secure.travis-ci.org/jolira/superpom.png" />](http://travis-ci.org/#!/jolira/superpom)
=========================

SuperPOM for all your maven components. Requires GPG code-signing.

To run, use

```
mvn release:prepare release:perform \
      -DperformRelease=true \
      -Dgpg.passphrase=password
```

Details about working with GPG can be found at http://www.sonatype.com/people/2010/01/how-to-generate-pgp-signatures-with-maven/
