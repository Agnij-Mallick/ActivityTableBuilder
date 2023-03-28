# ActivityTableBuilder

The Activity Table Builder is a tool generate an activity table to demonstrate Process Mining to someone starting out in the field.
It generates a simple activity table with sorting, case ID, activity, and timestamp.

(Work in Progress - the entire README will be up and ready soon.)

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
    <img src="https://github.com/Agnij-Mallick/ActivityTableBuilder/blob/f1ed2bb9c3520708dde68012d36361b0861cd62a/images/img1.png" alt="Locate Machine Learning in the left panel in the Data Option" style="height: 500px; width:211px"/>
</p>

Create a new Workbench.

<p align="center">
    <img src="https://github.com/Agnij-Mallick/ActivityTableBuilder/blob/807eb51a588cbad8d064e828ba81c061a97bbfdc/images/img2.png" alt="ML Workbench" style="height: 148px; width:470px"/>
</p>

The Workbench does not require any permissions to be granted to it.

### Setting up the Workbench
Once the Workbench has been created, launch it and open the terminal.

<p align="center">
    <img src="https://github.com/Agnij-Mallick/ActivityTableBuilder/blob/807eb51a588cbad8d064e828ba81c061a97bbfdc/images/img3.png" alt="Terminal in ML Workbench" style="height: 338px; width:960px"/>
</p>

Install the `DateTime` package with `pip`. Type the following in the terminal and press return.

```
pip install DateTime
```

<p align="center">
    <img src="https://github.com/Agnij-Mallick/ActivityTableBuilder/blob/54afec166e18fc88063d6e8fb1a68c824b52a53d/images/img4.png" alt="Terminal screenshot" style="height: 145px; width:960px"/>
</p>

All other dependencies are installed by default in the EMS. However, if you are using an offline installation of Jupyter Notebook install the following packages:

1. `pandas`
2. `numpy`
3. `random2`
4. `python-dateutil`

### Cloning the repository


### Set up the Activity List


### Running the Tool


# Congratulations! You have generated your own activity table!

## Things to look out for
### Using the correct Delimiter for your CSV file


### Editing the file to work with EMS


### Maintaining the Template