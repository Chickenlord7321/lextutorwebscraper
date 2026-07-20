# Lang Extractor

This script is for use by the Linguistics Research Lab at VIU. It extracts specific language characteristics from the 
website https://www.lextutor.ca/vp/comp/ and puts the data into a CSV file called extracted_data.csv.

## Text file Naming Format

- All text files must be named in the format "XXX_JD_QX_70db.txt"
- Where:
  - XXX is the 3-digit subject ID;
  - JD is the initials of the experimenter;
  - And QX is the question number (X is a number from 1 to 15).
  - e.g. 004_YM_Q1_70db.txt

## Download the Code

If you know how to use git comfortably, run:
```bash
git clone https://github.com/Chickenlord7321/lextutorwebscraper.git
````

Otherwise, click the green code button, choose _download ZIP_, and open the ZIP file. The remaining steps assume that 
you are operating from inside the **lextutorwebscraper** folder.

## Setup

1. Create a folder called **"textdata"** in the same directory of the main.py
2. Place all the txt files in the **textdata** folder
3. Now, depending on which OS you are using:

> ### Windows
> 
> - If you are on **Windows**, download the latest version of the chrome driver from https://googlechromelabs.github.io/chrome-for-testing/ or the version corresponding to your Google chrome version and place it in the same folder as main.py. 
>  - Make sure the chrome driver is named "**chromedriver.exe**"
>  - Most likely you will need the **chromedriver | win64** version, but be sure to double-check which version of Windows you are running. 
 
> ### MAC or Linux
>
> - If you are on Linux or Mac, download the latest version of the Firefox gecko driver from https://github.com/mozilla/geckodriver/releases.
>  - For example, if you are on a Macbook, you will want to download and open "**geckodriver-v0.37.0-macos.tar.gz**" (0.37 is the latest version as of writing).
>  - Make sure the driver file is named "**geckodriver**"

4. If you are not in PyCharm already, open the lextutorwebscraper folder in PyCharm now. 
   - You can do this by clicking on the PyCharm desktop icon, then...
   - Click the icon with 4 horizontal lines in the top left corner, which opens the file options
   - Click "Open..."
   - Choose the "lextutorwebscraper" folder and click "OK"
   - Now, to run any of the following bash commands, you can just click the green arrows that appear next to each command.


5. Create a virtual environment

```bash
python3 -m venv venv
```
6. Activate the environment

```bash
source venv/bin/activate
```

7. Install the required packages

```bash
pip install -r requirements.txt
```

## Running the Script

Simply run the script

```bash
python3 main.py
```

You will be prompted to choose one of two options:
1. Pressing "1" will add all the data from the txt files to the existing CSV file WITHOUT overwriting. It simply APPENDS the data.
2. Pressing "2" will OVERWRITE the CSV file entirely with the new data.
3. Pressing any other key will quit the program immediately.

The program will then run for a few seconds up to several minutes. Don't worry if it seems to be "doing nothing" at first, this is normal.

If the program has not brought up the webpage within 30 seconds, **press CTRL + C to quit the program.**

Finally, a CSV file called **extracted_data.csv** will appear in the same folder as main.py
