# multivagenv
This Script is to spin up several VM envs with optional values to input.
To run the script use the following command vagrant up to spin all the VM's and this applies to every command except when you specify the name of the VM.
Use vagrant global-status to show all the VM you have even if they have been deprecated.
Use vagrant global-status --prune to prune out deprecated VM's.
# Use Vagrant suspend to keep or save your env at the current state and vagrant reload to bring it back up.
# Use Vagrant halt to shutdown your VM and use vagrant up to bring it up
# Then use vagrant destroy to destroy the VM env.
# Use vagrant reload --provision anytime you make changes to the provision section of the vagrant file if the vagrant VM is already in a running state otherwise use vagrant up if it's not in a running state.
# If you want to mount a folder from the host machine say from your windows latop to your vagrant VM, use double backward slash, \\ to separate your paths otherwise it will throw you an error. For instance I want to mouunt a script I wrote that is on my windows machine that's located on this path C:\Users\myshellsh to this path on my vagrant vm /opt/scripts, I will make changes to the shared or synced folder in the config shared folder to look or be like this config.vm.synced_folder "C:\\Users\\myshellsh", "/opt/scripts". This implies that whatever you have on the C:\Users\myshellsh will auto be seen in /opts/scripts in the VM. This also offers the advantage that if peradventure your VM becomes corrupted or deleted by mistake, you can always spin another VM and mount the same folder from your host machine hence you don't lose your folder or data that you saved in that path.
