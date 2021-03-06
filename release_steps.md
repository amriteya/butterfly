# Release steps

1. Working from develop branch:
   1. Rev up all 9 pom files to the release version
   1. Build and test it
   1. javadoc
      1. generate javadocs for utilities and extensions-api projects: `mvn javadoc:javadoc`
      1. place javadocs files under `docs/javadocs/<version>`
      1. update links in `Extension-development-guide.md`, pointing to latest javadoc
      1. commit only javadocs `Adding javadocs for version x`
   1. doc
      1. update zip link in `Installing-Butterfly.md`
   1. Update release notes
   1. Push changes `Releasing x` (deployment will be done automatically by CI job)
1. Manual sonatype release
   1. Staging Repositories
   1. Close (the one with sources and everything)
   1. Release
1. Send and merge PR from develop to master
1. tag new release
1. Close milestone
1. Working from develop branch:
   1. Rev up all 9 pom files to the next SNAPSHOT version
   1. Add new version empty section in release notes
   1. Push changes
1. Create new milestone
1. Add issues to new milestone (if any)