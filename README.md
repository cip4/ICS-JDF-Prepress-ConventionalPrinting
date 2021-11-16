# ICS-JDF-Prepress-ConventionalPrinting
ICS for JDF Prepress to Conventional Printing

This ICS describes the minimum requirements for a solution to be conformant to the interface between a Prepress system and a Conventional Press print manager

<br />

## Issue Tracking
TBD

<br />

## Development Notes
### Release a new Version
Creation and publishing of a new version to GitHub Release. 

```bash
$ git tag -a ICS-JDF-MIS-ConventionalPrinting-[VERSION] -m "[TITLE]"
$ git push origin ICS-JDF-MIS-ConventionalPrinting-[VERSION]
```

In case a build has been failed, a tag can be deleted using the following command:
```bash
$ git tag -d ICS-JDF-MIS-ConventionalPrinting-[VERSION]
$ git push origin :refs/tags/ICS-JDF-MIS-ConventionalPrinting-[VERSION]
```

### Build Artefacts
Each build process produces a single PDF. This is either a release version for public distribution, or a continuous integration (CI) build for use

### Build Process

CI builds are triggered by any 'push' to the [MASTER] branch.<br/>
There is an option to trigger this build manually in the event that an automated CI build fails due to issues with the build process.

Release builds are triggered by adding a git tag to a commit. The value of tag will be used as the document identifier on both the cover and in the resulting artefact file name.<br/>
For example use a tag of 'Draft-IP-4' or 'Version 2.1 Final'.<br/>
There is alos an option to trigger this build manually.

