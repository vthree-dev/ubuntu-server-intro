# ubuntu-server-intro

introduction to basic function and usage of ubuntu server.

## [for windows-only user] git-bash
If you have only windows machine, you will have lots of troubles with server but you can still get most of functionality with e.g. git-bash. Install git-bash following [here](https://git-for-windows.github.io) and open your git-bash when I say **terminal** in all following sections.

## [optional] use AWS
If you don't have server access or you are required to manage servers: 

[Learn to use AWS here](https://github.com/griffithlab/rnaseq_tutorial/wiki/Intro-to-AWS-Cloud-Computing)

It's basically free if you use it carefully. 

**STOP a server** from AWS console if nobody is using it. 

**You are charged** even if you disconnect from server.

## connect
open your terminal, and type in command `ssh [username]@[server.address]` and press enter

e.g. `ssh baian@ec2-**-**-***-***.us-east-2.compute.amazonaws.com`

Type in your password when it prompts out.

When you see a banner at the top of your terminal and a new interface, you are successfully connected.

## never do these
Once you are connected, please be sure that you should never do these unless you fully understand what you are doing.
1. type in anything containing `sudo`
2. `rm ~ -r`
3. `rm * -r`
4. touch anything related to `ufw`
5. touch anything related to `apache` or `apache2`
6. [to be continued]

## config your account
type in `passwd` and press enter to change your password

use `chfn` to change other less important config, see [here](http://manpages.ubuntu.com/manpages/trusty/man1/chfn.1.html) for options and details

## intro to linux (ubuntu)
execute following commands line by line if you have totally no idea what you are doing and where you are and need some basic taste of the server
```
ls
mkdir test
ls
cd test
ls
ls ..
cd ..
ls
ls test
cd .
ls .
pwd
cd test
pwd
cat a>a
ls
cd a
ls
pwd
rm a
cd ..
rm test
rm -d test
```

read [this](http://www.tldp.org/LDP/intro-linux/html/)(at least section 2 and 3) carefully

use `man [command]` (e.g. `man pwd`) to get help (use `q` to exit)

## [optional] intro to shell
[here](http://www.shsu.edu/~csc_tjm/cs431/shellprog.html)

## vim
Vim is **THE** editor if you are editing files on server.

`man vim` to have some basic ideas

`vimtutor` and finish the tutorial (at least lesson 1 and lesson2)

## tmux
Use tmux to manage windows in terminal. Run process on server with tmux to safely disconnect. 

create new window: `tmux`

attach to a window: `tmux a`

detach from window: `ctrl+b d`

switch between windows: `ctrl+b s`

split window: `ctrl+b %` and `ctrl+b $`

## [optional] environment?
read [this](https://wiki.archlinux.org/index.php/environment_variables) carefully
