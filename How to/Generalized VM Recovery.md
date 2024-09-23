# Problem
You may have faced a situation where you tried to create an image of Azure VM, then then no longer able to run that original VM. This is because when you use a VM to create an image the disk of that image is templatised and all VM specific data is deleted. There is no way to recover this action.

Once generalize the VM, no further actions on it are allowed. For example, a generalized virtual machine can't be started or modified. If you do not generalize the virtual machine, you can continue to use it as normal.

# Resolution
If you want to recover you previous VM one option is to create a new VM using the disk that was attached to that VM. You can follow the instructions below;

1. In Azure portal go to "Disks" page.
2. Search for the disk that was atached to your VM.
3. Choose disk and select "Create Snapshot". Enter the data as required and create a snapshot of the disk.
4. Go back to the "Disks" page. Click "Create".
5. Enter the data as required in the "Create a managed disk" page. In the "Source type" select "Sanpsot".
6. In the "Source snapshot" select the snapshot of the disk you created in step 3.
7. After the new disk is created click "Go to resouce" or go the the disk that was created.
8. Click "Create VM".
9. Enter the data as required and create a new VM. Make sure the disk that was created in the previous steps is selected in the "Image" field.
10. Create VM.

# Verification
Then you are done. Next, connecto to your VM and chek if everything is intact. You should have all user profiles, the programs you installed and even the browser shortcuts you have in you previous VM.
