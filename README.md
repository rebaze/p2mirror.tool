# p2mirror.tool
Standalone Eclipse Mars based P2 Mirror Application

# Installation

## Install with Homebrew

Just `brew tap rebaze/repo` and then `brew install p2mirror`.

If the formula conflicts with one from Homebrew/homebrew or another tap, you can `brew install rebaze/repo/p2mirror`.
	
## Install as download

Grab latest from [https://ci.rebaze.io/nexus/#nexus-search;gav~com.rebaze.eclipse.p2mirror~~~~macosx]
	
	
# Usage

## Mirror P2 Metadata
	$ p2mirror -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source https://bndtools.ci.cloudbees.com/job/bndtools.master/lastSuccessfulBuild/artifact/build/generated/p2 -destination file:/tmp/out
    
## Mirror P2 Artifacts
    $ p2mirror -nosplash -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source $P2SRC -destination $P2DEST
  
Source can be any P2 repo. Destination is a local file url that you want to mirror to.

# Examples:

Mirror the Eclipse Neon P2 Repository to folder /data:

    ./p2mirror -nosplash -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source p2mirror -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source http://download.eclipse.org/releases/neon -destination file:/Users/tonit/neonmirror -destination file:/data

Mirror the BNDTools P2 Repository (latest build) to  folder /data:
    
        ./p2mirror -nosplash -verbose -application org.eclipse.equinox.p2.artifact.repository.mirrorApplication -source https://bndtools.ci.cloudbees.com/job/bndtools.master/lastSuccessfulBuild/artifact/build/generated/p2 -destination file:/data
    