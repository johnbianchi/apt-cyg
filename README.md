apt-cyg
=======

A command-line software installer for Cygwin.
Original version is available in http://code.google.com/p/apt-cyg/.

Recently, Cygwin mirror sites change their directory structure,
and original apt-cyg doesn't work on them anymore.

In this repository, an updated version of apt-cyg which can be used for
the new Cygwin mirror site strucuture is available.


## Example installation

    $ cd /tmp; git clone git@github.com:paprykarz/apt-cyg.git
    $ cp apt-cyg/apt-cyg /bin/ # or wherever in your $PATH 
    # If you want to get bash completion, include completion mechanism from .bash.d/completions/apt-cyg
    # You can include it statically, by sourcing script into current shell, e.g in. ~/.bashrc
	. .bash.d/completions/apt-cyg # suppose that directory .bash.d/completions/ exists 
    # or dynamically via completion loader function.
    $ rm -rf apt-cyg # if the local repository is not necessary

## Usage
2013-09-26:
Find: two new options: --ignore-case, --available-only
Added primitive completion of parameters and available packages

13/08/2013 update:
This version can be used exactly same way with original apt-cyg.
Architecture will be set automatically.

If you want to specify mirror site, put x86 (for 32 bit machine) or x86_64 (for 64 bit machine) at the end of URL

    $ apt-cyg update -m ftp://mirror.mcs.anl.gov/pub/cygwin/x86_64/
