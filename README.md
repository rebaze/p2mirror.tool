# p2mirror.tool
Standalone Eclipse Mars based P2 Mirror Application

# Installation

## Install with Homebrew
	brew install p2mirror
	
## Install as download

Grab latest from [https://ci.rebaze.io/nexus/#nexus-search;gav~com.rebaze.eclipse.p2mirror~~~~macosx]
	
	
# Usage

## Mirror P2 Metadata
	$ p2mirror p2mirror -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source https://bndtools.ci.cloudbees.com/job/bndtools.master/lastSuccessfulBuild/artifact/build/generated/p2 -destination file:/tmp/out
    
## Mirror P2 Artifacts
    $ p2mirror -nosplash -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source $P2SRC -destination $P2DEST
  
Source can be any P2 repo. Destination is a local file url that you want to mirror to.

# Examples:

Mirror the BNDTools P2 Repository (latest build) to  folder /data:

    ./p2mirror -nosplash -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source https://bndtools.ci.cloudbees.com/job/bndtools.master/lastSuccessfulBuild/artifact/build/generated/p2 -destination file:/data
