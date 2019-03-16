# bash.scripts
Some useful bash scripts

* `bundleFiles` will combine all the files whose names are given as arguments
  and will combine them into a single file called `bundle.out` which can then
  be edited to make changes to all the files in one go. The `bundle.out` file
  is an executable shell script which when run will unpack all the files into
  their original versions with the changes applied. You can copy the
  `bundle.out` file before editing it as a backup. You should remember to
  delete any unwanted `bundle.out` files when you have finished with them.
* `shout.alert` will print its arguments as a standard alert message to
  standard out
* `shout.header` will print its arguments as a standard header message to
  standard out
* `shout.short` will print its arguments with leading stars to standard
  out. Each argument is printed on a separate line with the second and
  subsequent lines having a greater indent than the first.
* `shout.smallHeader` will print its arguments as a smaller header message to
  standard out
* `makeQScript` will take the name of a file containing shell commands to be
  run and will generate a second file with the name of the first file plus
  `.QScript`. This new file will have each line surrounded with shell
  commands that will prompt you to confirm that you want to run the command
  before running it.
* `semVerLatest` when run within a git repository will print the highest
  semantic version ID. **NOTE:** You must have the `semvertools` commands
  somewhere in your PATH
* `semVerList` when run within a git repository will list all the tags on the
  repository correctly sorted as semantic version IDs. **NOTE:** You must
  have the `semvertools` commands somewhere in your PATH
* `semVerNext` when run within a git repository will find the highest valid
  semantic version number and increment it. By default it will increment the
  patch version but you can supply arguments to change this: `-part minor`
  will increment the minor version and `-part major` will increment the major
  number. **NOTE:** You must have the `semvertools` commands somewhere in
  your PATH
* `semVerUpdGoModToLatest` when run within a git repository will find the
  latest versions of the required modules and prompt you to upgrade to
  them. **NOTE:** You must have the `semvertools` commands somewhere in your
  PATH
* `YNQ.func` is a function definition that can be loaded into scripts and it
  provides a utility function that prints a prompt, reads a reply and
  optionally executes a command. According to the value of the reply it will
  either skip the command, quit the script or run the command.

## Installing the scripts
First get these scripts from git

`git clone ssh://git@github.com/nickwells/bash.scripts`

At this point the scripts will not have the execute bit set so there is a
script provided that you can dot into your shell in order to make the scripts
executable. It will also check that some of the tools needed have also been
installed and warn you if not. Run the initialise script as follows:

`. initialise.bash.scripts`
