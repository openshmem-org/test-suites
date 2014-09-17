test-suites
===========

Meta collection of vendor test suites.  This repository does not contain any of these suites, but instead manages a form of link to each of the individual repositories containing them.  These links reference a specific commit id (not a branch) of a target repository.  This can be used to get the latest known "good" versions of the suites for testing, but changes to any of the suites themselves still needs to be done within the different suite's respective repositories.  Some useful commands for managing this repository of repositories are outlined below.

`git clone` - Create a local copy of this repository.  This will not connect to or pull from any other repositories.

`git submodule init` - After cloning, be sure to run this command to initialise the url links for each test suite to that from the .gitmodules file so that git can find each of the other repositories (submodules) being managed.  This only needs to be run once.

`git pull` - When in the top level of this repository, this is needed to pull in the latest links to the various test suites.  If done inside a submodule's directory, it will instead only attempt to pull that suite's latest changes.

`git submodule update` - After a checkout or (top level) pull, run this to check out the commit referenced by the submodule link for each test suite.  Git will automatically pull any remote objects needed from the appropriate repositories.
