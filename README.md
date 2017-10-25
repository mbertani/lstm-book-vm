# lstm-workshop-vm
A virtual machine Deep-learning-ready for the book [Long Short-Term Memory Networks With Python](https://machinelearningmastery.com/lstms-with-python/)

## Setup

1. Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. Install [Vagrant](https://www.vagrantup.com/)
3. If you have Git, clone this repository. Otherwise download the content as a ZIP archive and unpack it somewhere.
4. Open a command line interface/shell (PowerShell or Cmd on Windows, Terminal on Mac, your favourite terminal emulator on Linux)
5. Change directory to the location of this repository's files.
6. Run: `vagrant up --provision` the first time you start up the VM. Use just `vagrant up` for subsequent calls.
7. Get some coffee, eat a sandwich or surf the web or something, this will take about 10 minutes depending on your internet connection and computer.
8. Run `vagrant ssh` to log onto the VM from the shell. 
9. Inside the box, run `./run_jupyter.sh` to start the jupyter notebook server.
10. Open your browser at [http://localhost:8888](http://localhost:8888) and log in with password `workshop`
11. When you want to stop the VM, use `Ctrl+c` to stop the server, then `exit` to leave the ssh session, and `vagrant halt` to stop the VM.

## Notes

### RAM

The VM has 2 GiB of RAM by default. If you want to increase performance, you may increase the `v.memory` in [Vagrantfile] to about half of what you have on your system. DO NOT SET THIS HIGHER THAN 75% OF YOUR SYSTEM'S RAM.

### CPUs

The VM has 2 cores by default. If you want to increase performance, you may increase the `v.cpus` in [Vagrantfile] to half of the number of logical cores on your system. DO NOT SET THIS HIGHER THAN HALF THE NUMBER OF LOGICAL CORES ON YOUR SYSTEM.