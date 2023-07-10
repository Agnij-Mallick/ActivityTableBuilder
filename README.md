# ActivityTableBuilder

The Activity Table Builder is a tool generate an activity table to demonstrate Process Mining to someone starting out in the field.
It generates a simple activity table with sorting, case ID, activity, and timestamp.

## Preparation

### Software

If you are already signed up for [Celonis Execution Management System](signup.celonis.com), you can use the Machine Learning Workbench to build your activity table. Alternatively, you can also use an offline installation of Jupyter Notebook. If you are using an offline installation of Jupyter Notebook, it is recommended that you also have a spreadsheet editor available to you.

### Building a Scenario

Before you start building a scenario, think about how you would like the scenario to look like. Some of the questions you would want to ask yourself are:
1. What is the context behind the scenario?
2. What are the possible activities that can happen when there are hundereds of instances of the scenario playing out?
3. What is my 'happy path'?
4. What are the possible variants?
5. What other information you will need to build an analysis?

### Building a Case Table

This tool exclusively builds activity tables. Since case tables can vary significantly between scenarios, it is recommended that each case table is build out to suit its intended purpose.

## Generating an Activity Table
### Accessing the Machine Learning Workbench

Go to Machine Learning in Data Integration.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img1.png" alt="Locate Machine Learning in the left panel in the Data Option" style="height: 500px; width:211px"/>
</p>

Create a new Workbench.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img2.png" alt="ML Workbench" style="height: 148px; width:470px"/>
</p>

The Workbench does not require any permissions to be granted to it.

### Setting up the Workbench
Once the Workbench has been created, launch it and open the terminal.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img3.png" alt="Terminal in ML Workbench" style="height: 338px; width:960px"/>
</p>

Install the `DateTime` package with `pip`. Type the following in the terminal and press return.

```
pip install DateTime
```

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img4.png" alt="Terminal screenshot" style="height: 145px; width:960px"/>
</p>

All other dependencies are installed by default in the Workbench. However, if you are using an offline installation of Jupyter Notebook install the following packages:

1. `pandas`
2. `numpy`
3. `random2`
4. `python-dateutil`

### Cloning the repository

Clone the repository into the Workbench. Use the following command in the terminal:

```
git clone https://github.com/celonis-content/ActivityTableBuilder.git
```

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img13.png" alt="git command" style="height: 153px; width:960px"/>
</p>

### Set up the Activity List

Once the repository has been cloned into the workbench, navigate to the ActivityTableBuilder folder. Open the file "activity_list.csv". It is a template for the input file.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img6.png" alt="activity_list" style="height: 163px; width:960px"/>
</p>

If the file does not appear as the above picture, try changing the delimiter to ";".

#### Downloading a File from ML Workbench

If you have not downloaded a file from the Machine Learning Workbench previously, your first download will be an HTML file.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/8f42145b349d0cb1f6a7258a44170896a0c8f0b3/images/img17.png" alt="editor" style="height: 76px; width:232px"/>
</p>

Open the file. It will redirect you to another webpage. Scroll down, check *Don't show this again* and click on *Download File*.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/8f42145b349d0cb1f6a7258a44170896a0c8f0b3/images/img18.png" alt="editor" style="height: 290px; width:507px"/>
</p>

Try downloading the file again.

#### **Editing the File**
Either download the file on to your system or use the Editor in the Workbench.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img10.png" alt="editor" style="height: 319px; width:275px"/>
</p>

If you download the file to edit it, delete the temnplate from the folder and upload the filled in file **without renaming it**.

#### **FIlling up the Activity List**

**Column 1:** The first column is a list of all the possible activities that can happen during the process.

**Minimum Duration & Maximum Duration:** The second and third column denote the minimum and maximum time in hours an activity can take to be completed respectively.

**END:** This is a flag to denote whether an activity is a terminal activity, i.e., the process can end at that activity. If an activity is a terminal activity then the value is 100, otherwise 0.

**Column 5 and beyond:** These columns denote the probability of an activity in row 1 being following an activity in column 1. E.g.

If Activity 2 follows Activity 1 in 80% of the cases, then the entry at the intersection of Activity 1 in Column 1 and Activity 2 in Row 1 should be 80.

*N.B.:* Ensure that the sum of the entires in a row from 'END' (inclusive) onwards adds up to 100.

### Running the Tool
Once the "activity_list.csv" is filled up, open the "Run_ActivityTableBuilder.ipynb" file.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img14.png" alt="JP Notebook" style="height: 175px; width:145px"/>
</p>

Move your cursor to the code block.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img15.png" alt="JP Notebook" style="height: 500px; width:960px"/>
</p>

Run it by pressing **Control**+**Return**.

You will be required to enter the number of cases you want to generate. While there is no restriction on the number of cases you can generate, the Academic License of the EMS can only allows 100,000 rows in a table by default.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img16.png" alt="JP Notebook" style="height: 500px; width:960px"/>
</p>

# You have generated your own activity table!
Your activity table should be generated. It will appear in the file explorer in the Workbench.

## Things to look out for
### Using the correct Delimiter for your CSV file
The template file uses ";" as the delimiter in the CSV file. If you use an offline spreadsheet tool to edit the template, make sure to check whether the demiliter matches between the code and file.

<p align="center">
    <img src="https://github.com/celonis-content/ActivityTableBuilder/blob/d8d7a18ef495acfca04e31446025713e8e29f130/images/img11.png" alt="Delimiter" style="height: 70px; width:670px"/>
</p>

### Editing the file to work with EMS
The cell of the activity table generated at the 1<sup>st</sup> row, 1<sup>st</sup> column is empty. This will result in an error when uploading the the EMS using Upload Files option in a Data Pool. Rename this cell to "Sorting".

### Maintaining the Template
The program is dependent on the template being maintained. Changing the layout of the Activity List file will result in the program not working as expected.
