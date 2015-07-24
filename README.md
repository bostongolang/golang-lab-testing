# Golang Boston Lab #2 - Testing

Welcome to the second Boston Go language lab! 

The goal of this lab is to practice writing tests by create some unit tests for some open source projects.

We have identified some projects in the [projects/](/projects) folders with instructions.

## Prerequisites 

1. PLEASE BRING:  A laptop with a Go language environment with Go 1.4 already set up. Please see 'Vagrant setup' below to get started with one easily.
  * If you are having trouble setting up your Go programming environment, please join the #lab-help channel in the Boston Golang Slack group. You can signup for the Slack group [here](http://bostongolang-slack-invite.herokuapp.com/).

2. PLEASE BRING: A text editor or IDE suitable for writing Go code.
  * For beginners, [Sublime](http://www.sublimetext.com) is a good option. Make sure you install the Go plugin [here](https://github.com/DisposaBoy/GoSublime).
  * For VIM users, there is a pretty nice VIM setup [here](https://github.com/fatih/vim-go).  

3. PLEASE HAVE:  Some basic Go language exposure.  You should be familiar with the Go basics: e.g., Go's types, structs, control flow structures, goroutines, and channels.   
Other programming language experience and concepts (such as networking, etc) will be helpful. A good introduction to the basics of Go for people familiar with 
other programming language is available at: [https://tour.golang.org](https://tour.golang.org). If you can get through this tour, you will be well-prepared for this meetup!

### General setup

1. Fork this repository in Github.

1. Clone the repository into a directory
  
  ```bash
  # open a terminal window and type:
  $ git clone https://github.com/bostongolang/golang-lab-testing.git
  ```

### Vagrant setup

1. Install [Vagrant](http://www.vagrantup.com/downloads) for your platform.
1. Open a terminal window, and cd /path/to/this/repository.

  ```bash
  # open a terminal window and type:
  $ cd golang-lab-chat
  ```

1. From within the `golang-lab-chat` directory, type `vagrant up`. This will create a virtual machine with Ubuntu linux and Go 1.4 installed for the Vagrant user.
1. Type `vagrant ssh` to ssh into the virtual machine.  

Within the virtual machine, `golang-lab-chat` on the host computer
will be mapped to /opt/golang-lab-chat in the guest.  So any changes
you make in the normal filesystem should be reflected in the VM!

Need help? Arrive a little early and we can help you get up-and-running, or join
the Boston Golang Slack group #lab-help channel group by signing up [here](http://bostongolang-slack-invite.herokuapp.com/).

You can also email me directly: [jandre+bostongolang@gmail.com](mailto:jandre+bostongolang@gmail.com).

## Projects

TBD


