# exoslam-tutorial
Notebook and code for JWST analysis tutorial at exoSLAM 2025.

## Pre-Tutorial Setup Instructions
The following is important setup information for the JWST data analysis tutorial and needs to be completed **before** coming to the tutorial! You may encounter some issues, especially if you are new to programming and there will not be time during the tutorial to do this!

If you encounter difficulties with the installation steps, the easiest thing to do is to post an issue on the tutorial’s GitHub page here: https://github.com/radicamc/exoslam-tutorial/issues describing your issue. The earlier you do this, the better chance someone has of being able to help!

0. If using Mac or Linux, ignore this step. If you have a Windows machine, your life is going to be more difficult. You’re first going to need to install a linux distribution on your windows machine to make sure everything runs smoothly. The recommended way to do this is with Windows Subsystem for Linux: https://learn.microsoft.com/en-us/windows/wsl/install. Once you have WSL set up (the default ubuntu linux distribution should be fine), you can proceed with the rest of the setup. 
1. Install anaconda – this is going to be our preferred way of accessing python. Follow the steps here: https://www.anaconda.com/docs/getting-started/anaconda/install#linux-installer to install the appropriate version of anaconda for your OS. Note if you are using WSL installed above, you’ll need the Linux installer. 
2. Create and set up a conda environment for this tutorial.    
    1. Open your terminal.
    2. Create an anaconda environment using python 3.10, something like the following
         command should work fine:   
       ```conda create -n “exotedrf-tutorial” python=3.10```
    3. Activate your new environment:   
       ```conda activate exotedrf-tutorial```
    4. Install the package manager pip (if not automatically installed):  
       ```conda install pip```
3. Install exoTEDRF:   
    ```pip install exotedrf --no-cache-dir```
4. Create a jupyter kernel from your new environment:   
    ```python -m ipykernel install --user --name=”exotedrf-tutorial”```
5. Clone the tutorial GitHub repository:     
    ```git clone https://github.com/radicamc/exoslam-tutorial```  
Mac users may need to install developer tools at this point if you have never used git before. 
6. Check that everything works.
    1. Enter into the tutorial directory:  
    ```cd exoslam-tutorial``` 
    2. Run the test script:  
    ```python test_script.py```  
If the script ran to completion and printed out something like the following:  
		```2025-06-25 12:24:01.752 - exoTEDRF - INFO - Teddy bears!```  
then you’re all good to go!
Note that the date and time shown will depend on when you run this command.  
Mac users, if you see the following error:  
    ```RuntimeError: cannot load _umath_tests module```  
at this stage, you simply need to change your installed version of numpy from the default:  
	```pip install numpy==1.24.3```  
Pip may throw you warnings that this version of numpy is incompatible with some other packages, but you can ignore that.  
7. Download the tutorial data files (~7Gb) from box here: https://uchicago.app.box.com/s/ezx57mwux6r1584efbv3i53fc9aot1oq. Unzip the file (if not done already) and place the resulting folder in the tutorial directory.


