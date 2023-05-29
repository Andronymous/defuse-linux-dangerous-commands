# Defuse Linux Dangerous Commands
This script helps defuse dangerous commands from your bash history.

Sometimes you and your colleagues work on the same server simultaneously. Due to the common habit of using the up key to find previous commands, there is a risk of mistakenly selecting and executing dangerous commands, such as rebooting or clearing a folder, from the history list. This script allows you to specify keywords for dangerous commands, which will then be modified in the command history. By running this script in your .bashrc file, you can ensure safer command execution.

How to Use
------------------
Follow these steps to use the script on an Ubuntu or any Debian-based system:

1.Copy the file defuse-dangerous-commands.sh to any directory of your choice.

2.Edit the KEYWORDS field in the script and add any command keywords that you consider dangerous.

3.Link your shell login to run the script every time you log in to the user. For example, in Ubuntu, open a terminal and log in to the user for whom you want to defuse the commands.

4.Edit the user's .bashrc file located at ~/.bashrc and add the following command at the end of the file:
```
bash /path/of/the/file/defuse-dangerous-commands.sh
```
Replace /path/of/the/file with the actual path where you copied the script file.

5.Save the .bashrc file and exit the text editor.

6.That's it! Whenever a user executes a dangerous command in their bash session and the command is saved in the session history file,When another user logs in to a different session, the script will be applied and will modify the command in the form dangerous-command [command] to prevent accidental execution.
```
dangerous-command [command]
```
to prevent accidental execution of potentially harmful commands.

Feel free to customize the script according to your needs and add any additional dangerous command keywords to the KEYWORDS field.

