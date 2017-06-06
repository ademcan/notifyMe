# notifyMe

This script will send an email once a job started on an SGE-based cluster is finished. 
By default SGE system supports email notification. However, sometimes this option is not implemented.

## How to use

1. Clone the repository in your ~/bin folder (or any other folder you like)
```
cd ~/bin
git clone https://github.com/ademcan/notifyMe
```
2. make notifyMe executable (in case it isn't yet)
```
cd notifyMe
chmod +x notifyMe
```
3. add your notifyMe directory to your PATH. The best is to add it to your .bashrc so you don't have to do this step everytime you connect.
```
export PATH=~/bin:$PATH
```
4. Updated your USERNAME and EMAIL address in the script (line 15)
5. Start your job (and add notifyMe to the command as follow):
```
qsub myjob.sh | notifyMe
```
6. Enjoy