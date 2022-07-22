# Instructions for setting up a new Windows computer

This repo is simply a `README.md` file that documents Stephen's
preferred way to set up a Windows computer. This repo is under
[Fossil](https://fossil-scm.org/) version control but is mirrored on
GitHub. The intendend audience is my future self or a new person on
the team.

## Install the Windows Terminal program

The Windows Terminal app is an improved terminal (or terminal
emulator) for Windows created by Microsoft. It allows you
to have multiple tabs open like a browser or split a window 
to see two terminal sessions at once.

Depending on your version of Windows it may already be installed. If
not it can be installed via the Microsoft Store.  Type "Microsoft
Store" in the search bar, to open the Microsoft Store app on your
computer and then search for "Windows Terminal".

## Install Scoop

[Scoop](https://scoop.sh) is a set of command line tools to make
installing and updating software easier. Scoop solves several
problems including making it easy to install and update software
with short commands and making it so the software can be easily
run from the command line. (For example, it solves common
problems associated with system paths.)


I did not document the steps for installing Scoop the first time I did
it but some instructions are here:
<https://github.com/ScoopInstaller/Install#

The Scoop Quickstart says to open up Windows Terminal and type this:

> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time
> Invoke-WebRequest get.scoop.sh | Invoke-Expression

The detailed explanation has these instructions:

> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> iwr get.scoop.sh | iex

Note that the second version is really the same; it uses `iwr` but
that is an alias for the longer `Invoke-WebRequest` and `iex` which is
an alias for `Invoke-Expression`.

The only difficulty one can expect is that one may need to get
administrator priviledges. If so this can be done through the Dock
(you can type "Dock" in the search bar) and then

- Click on the person in front of a folder icon
- Click Computer and Printer Settings and wait a while
- Click on Computer Privileges
- Click on Elevate My User Account

### Use Scoop to install additional programs

With Scoop successfully installed, one can enter the following
commands in the Windows Terminal program to get the next
set of programs.

```
PS> scoop help # This gives you more info on the commands below
PS> scoop update            # Updates scoop itself
PS> scoop install fossil    # Fossil is used for version control
PS> scoop install r         # We need R ...
PS> scoop install python    # ... and Python
PS> scoop bucket add extras # The "extras" bucket is needed for Geany,
PS> scoop install geany     # a simple code editor. Or try 'kate' or 'gedit'

```



