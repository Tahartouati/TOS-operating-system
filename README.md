# TOS-operating-system
 TOS is a simple operating system for Intel x86 based PCs, designed as a programming project to accompany a course on operating systems. At the end of the project, you will have implemented a small, pre-emptive multi-tasking operating system that can boot on any Intel-based PC. It controls an external model train via the serial line interface. The video below shows the result.

<h1>Getting Started with TOS</h1>

<p>
This page contains information to help you get started
with TOS.
Although TOS itself is relatively simple, compiling and running
TOS depends on a wide variety of tools. In particular, the following
freely available tools are required for TOS development:
</p>

<ul>
<li> GNU make and a native version of the GCC compiler.
</li><li> A version of the C compiler GCC that produces ELF binaries
for the Intel x86 architecture.
</li><li> The <a href="http://sourceforge.net/projects/nasm/">NASM</a> assembler.
</li><li> The <a href="http://bochs.sourceforge.net/">Bochs</a> PC emulator.
</li><li> <a href="http://www.python.org/">Python</a> to run the train simulator.
</li><li> To run the TOS Test Center (TTC), a Java Development Kit (JDK)
at least version 1.4.
</li></ul>

<p>
The only supported development platform for TOS is Ubuntu. If you do not
have a system running Ubuntu, you will need to install VirtualBox for your
environment and then install Ubuntu as a guest operating system within VirtualBox.
The next section provides instructions on how to run Ubuntu under VirtualBox.
The last section on this page describes how to download and install TOS once
Ubuntu is available.
</p>


<h3>Installing Ubuntu under VirtualBox</h3>

<p>
Compiling and running TOS requires the freely available Linux distribution
Ubuntu. It is recommended to use the desktop version of Ubuntu 16.04 LTS (64-bit).
Please use only this version and not newer versions of Ubuntu as TOS will
not work with newer versions!
If you have a development platform with this version of Ubuntu, skip to the next
section. If you do not have Ubuntu available, you need to install VirtualBox first.
VirtualBox is an industrial-strength Open
Source virtualization platform. VirtualBox is similar in spirit
to Bochs (that is used for running and testing TOS). However,
Bochs is a light-weight implementation suited for running TOS, while
VirtualBox is a powerful virtualization platform capable of running
Ubuntu as the guest operating system. The following steps explain
how to install VirtualBox on your platform and then install Ubuntu as the
guest of VirtualBox.

</p><ol>
<li> Download <a href="http://www.virtualbox.org/">VirtualBox</a>
for your platform.

</li><li> Download <a href="http://www.ubuntu.com/getubuntu/download">Ubuntu
16.04 LTS Desktop Edition (64-bit)</a>.

</li><li> Launch VirtualBox.

</li><li> Select: Machine &gt; New...

</li><li> Type "TOS Development" for the name. Select "Linux" for Operating
System. Select "Ubuntu (64 bit)" for Version.

</li><li> Leave the default for RAM size.

</li><li> Create a new Virtual Hard Disk. Select "Dynamically allocated".
Type "TOS Development" for Location. Select at least 8 GB of disk space.

</li><li> Click "Finish" to exit the new virtual machine wizard.

</li><li> On the main screen, click on Settings &gt; Storage. Select "Empty"
underneath of "Controller: IDE". Click on the CD icon on the right side
of the screen and select "Choose a virtual CD/DVD disk file..."

</li><li> Select the downloaded Ubuntu ISO image.

</li><li> Click on "Start" (the green right arrow) to start this virtual
machine.

</li><li> All the following instructions refer to the Ubuntu installation
process. Select "Install Ubuntu".

</li><li> Select your preferred settings (Language, time zone, keyboard layout).

</li><li> In the disk partitioner, let Ubuntu use the entire disk (default).

</li><li> In the following dialog, Ubuntu asks some details about the first
login.

</li><li> Confirm settings and let Ubuntu install itself. This will take a while.
At the end click on "Restart now".

</li><li> When Ubuntu reboots, it will tell you to remove the disk. At this
point simply exit VirtualBox (power-off option).

</li><li> Restart VirtualBox. Unmount the CD/DVD ROM. Restart Ubuntu.

</li><li> Once Ubuntu has finished rebooting, in VirtualBox select Devices
&gt; Install Guest Additions. You should see a CD icon on the Ubuntu
desktop.

</li><li> In Ubuntu, the auto-runner should automatically run the installation
script for the guest additions.

</li><li> Shutdown Ubuntu. Unmount the CD/DVD ROM. Reboot Ubuntu. You have
now completed the Ubuntu installation.

</li></ol>

<h3>Downloading and installing TOS</h3>

<p>
Once Ubuntu is available for TOS development, downloading and installing TOS
is simple. Open a shell and type:
</p>

<p>
<tt>curl -fsSL http://tos.sfsu.edu/dist/install-tos-prereqs.sh | sh</tt>
</p>

<p>
This script will download and install all required tools such as the gcc compiler
as well as the TOS skeleton code. Note that you will need to give the installation
script root privileges. Once the script has completed, you can test
the successful installation with the following instructions:
</p>

<ul>

<li> Open a shell.
</li><li> Type: <tt>cd tos;make tests</tt>
</li><li> Type: <tt>./run-ttc.sh</tt>
</li><li> Select <tt>test_mem_1</tt>
</li><li> Click the "Bochs" button.
</li><li> You should see one failed test.

</li></ul>

</div>
