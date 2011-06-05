SuperPOM for all your maven components. Requires GPG code-signing. To run, use 'mvn release:prepare release:perform -DperformRelease=true -Djavax.net.ssl.trustStore=${HOME}/.m2/.keystore -Dgpg.passphrase=password'. Details about working with GPG can be found at http://www.sonatype.com/people/2010/01/how-to-generate-pgp-signatures-with-maven/

