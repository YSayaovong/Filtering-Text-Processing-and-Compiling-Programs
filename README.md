# Filtering-Text-Processing-and-Compiling-Programs

PART 1: awk.

Open a new terminal window on your Linux system.
Type in ps and observe the output.
Type in ps | awk '{print}' and observe the output. It shouldn't impress you because it gave you the same output as the much shorter command in step 2 above, with the addition of showing awk as a process.
Type in ps | awk '{print $0}' and observe the output. It should be the same as step 3 above.
Now try this: ps | awk '{print $1}'
Then this: ps | awk '{print $2}'
Observe the output of steps 5 and 6 and try to determine what is going on with the output (i.e. what is awk doing?). 
Take a screenshot of the commands and output of steps 2-7. Name it lab_7_screenshot_1.
Type in man awk and review the manual page entry.
Type in clear.
Type in cat /etc/shells and observe the output.
Type in awk -F "/" '/^\// {print $NF}' /etc/shells and observe the output and compare it to the output of step 11 above.
Type in awk -F "/" '/^\// {print $NF}' /etc/shells | sort -u and observe the output and compare it to the output of step 12 above.
Take a screenshot of the commands and output of steps 11-13. Name it lab_7_screenshot_2.
PART 2: sed.

Clear your terminal window.
Type in echo "Large melons" > produce.txt
Type in echo "Large bananas" >> produce.txt
Type in echo "Small berries" >> produce.txt
Display the contents of produce.txt with cat.
Make a copy of produce.txt named produce.txt.bak in the same directory.
Type in sed -i 's/Large/Huge/' produce.txt
Display the contents of produce.txt with cat.
Type in diff produce.txt produce.txt.bak
Take a screenshot of the commands and output of steps 2-9. Name it lab_7_screenshot_3.
Clear your terminal window.
Type in sed -i '2s/Huge/Medium/' produce.txt
Display the contents of produce.txt with cat.
Type in sed -n '/bananas/=' produce.txt and note the output.
Type in sed -i '/bananas/i Medium oranges' produce.txt
Display the contents of produce.txt with cat.
Take a screenshot of the commands and output of steps 12-16. Name it lab_7_screenshot_4.
PART 3: Compiling programs from source code.

Clear your terminal window.
Type in git --version. It should say that git could not be found and tell you that you can install it with apt. We won't be doing that, instead, we will be installing git from source code.
Type in sudo apt install build-essential autoconf zlib1g-dev gettext -y. That will install everything you need to install software from source code. 
Type in cd /tmp.
Type in wget https://www.kernel.org/pub/software/scm/git/git-2.34.0.tar.gzLinks to an external site..
Type in tar -xzvf git-2.34.0.tar.gz.
Type in cd git-2.34.0.
Type in make configure.
Type in ./configure --prefix=/usr.
Type in make all.
Type in sudo make install.
Type in git --version to verify that git has been successfully installed from the source code package.
Take a screenshot showing that git has been installed (output is "git version 2.34.0) and ensure that you also capture a small portion of the output from the command that was run in step 11 above. Name the screenshot lab_7_screenshot_5.
