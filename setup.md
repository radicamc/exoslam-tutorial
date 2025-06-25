The following is important setup information for the JWST data analysis tutorial and needs to be completed **before** coming to the tutorial! You may encounter some issues, especially if you are new to programming and there will not be time during the tutorial to do this!

If you encounter difficulties with the installation steps, the easiest thing to do is to post an issue on the tutorial’s GitHub page here: https://github.com/radicamc/exoslam-tutorial/issues describing your issue. The earlier you do this, the better chance someone has of being able to help!

0. If using Mac or Linux, ignore this step. If you have a Windows machine, your life is going to be more difficult. You’re first going to need to install a linux distribution on your windows machine to make sure everything runs smoothly. The recommended way to do this is with Windows Subsystem for Linux: https://learn.microsoft.com/en-us/windows/wsl/install. Once you have WSL set up (the default ubuntu linux distribution should be fine), you can proceed with the rest of the setup. 
1. Install anaconda – this is going to be our preferred way of accessing python. Follow the steps here: https://www.anaconda.com/docs/getting-started/anaconda/install#linux-installer to install the appropriate version of anaconda for your OS. Note if you are using WSL installed above, you’ll need the Linux installer. 
2. Create and set up a conda environment for this tutorial. 
     a. Open your terminal.
     b. Create an anaconda environment using python 3.10, something like the following
         command should work fine:
conda create -n “exotedrf-tutorial” python=3.10
     c. Activate your new environment:
		conda activate exotedrf-tutorial
     d. Install the package manager pip:
conda install pip 
3. Install exoTEDRF:
	pip install exotedrf
Note: for those of you on Mac, you may need to also change the default installation of numpy to avoid some issues later on. This isn’t an issue with Linux, and I don’t know about Windows (but if you’re using WSL this should be taken care of). It may also just be a Mac silicon chip issue, but I cannot confirm or deny this.  
	pip install numpy==1.24.3
Pip may throw you warnings that this version of numpy is incompatible with some other packages, but you can ignore that.  
4. Create a jupyter kernel from your new environment:
	python -m ipykernel install --user --name=”exotedrf-tutorial”
5. Clone the tutorial GitHub repository:
git clone https://github.com/radicamc/exoslam-tutorial
6. Download the tutorial data files (~7Gb) from box here: https://uchicago.app.box.com/s/ezx57mwux6r1584efbv3i53fc9aot1oq. Unzip the file (if not done already) and place the resulting folder in the tutorial directory.
7. Check that everything works.
     a. Enter into the tutorial directory:
		cd exoslam-tutorial 
     b. run the test script:
python test_script.py 
If the script ran to completion and printed out something like the following:
		2025-06-25 12:24:01.752 - exoTEDRF - INFO - Teddy bears!
then you’re all good to go!
Note that the date and time shown will depend on when you run this command. 
