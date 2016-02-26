# p2mirror.tool
Standalone Eclipse Mars based P2 Mirror Application

# Usage:

    ./p2.mirror -nosplash -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source $P2SRC -destination $P2DEST
  
P2SRC can be any P2 repo. P2DEST is a local file url that you want to mirror to.

# Examples:

Mirror the BNDTools P2 Repository (latest build) to  folder /data:

    ./p2.mirror -nosplash -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source https://bndtools.ci.cloudbees.com/job/bndtools.master/lastSuccessfulBuild/artifact/build/generated/p2 -destination file:/data
