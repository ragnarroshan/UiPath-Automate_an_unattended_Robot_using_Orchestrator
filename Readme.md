## Exercise_12-Automate_an_unattended_Robot_using_Orchestrator

## Aim:

To automate the execution of an unattended robot process using UiPath Orchestrator, ensuring the process runs without human intervention.

## Equipment Required:

UiPath Studio (to design the process)<br>
UiPath Robot (to execute the process)<br>
UiPath Orchestrator (to schedule and monitor the process)<br>
A valid Orchestrator License and Robot license.

## Procedure:

### Step 1: Create a Process in UiPath Studio

Design your automation in UiPath Studio. For example, you can create a simple process like extracting data from a file and logging the results.<br>
After creatiing the process, publish it to Orchestrator:<br>
Click on Publish in UiPath Studio.<br>
Select Orchestrator as the destination.<br>
Choose a version number and click Publish.

### Step 2: Configure UiPath Orchestrator

#### 1. Log in to Orchestrator

Open UiPath Orchestrator in a browser.<br>
Sign in using your credentials.<br>

#### 2. Create a New Machine

Navigate to the Machines tab under the Tenant section.<br>
Add a new machine by clicking Add Machine.<br>
Provide a name for the machine (it should match the name used in UiPath Robot).<br>
Copy the Machine Key for later use.

#### 3. Configure UiPath Robot

Open UiPath Assistant or Robot on your machine.<br>
Click on Orchestrator Settings.<br>
Paste the Machine Key from Orchestrator.<br>
Provide the Orchestrator URL (e.g., https://cloud.uipath.com/your_account_name).<br>
Click Connect to link the robot to Orchestrator.

#### 4. Provision the Robot

Go to the Robots tab in Orchestrator.<br>
Click Add Robot and fill in the following details:<br>
Machine: Select the machine created earlier.<br>
Type: Select Unattended.<br>
Domain/Username: Enter the domain and username of the robot machine.<br>
Password: Provide the machine’s login password.<br>

### Step 3: Create and Deploy a Process in Orchestrator

#### 1. Create a Process

Go to the Processes tab in Orchestrator.<br>
Click Add Process.<br>
Choose the Package (the one you published from UiPath Studio).<br>
Select the Environment where the robot is deployed.<br>

#### 2. Assign a Robot to the Process

In the Processes tab, assign your unattended robot to the process.<br>

### Step 4: Schedule the Process

#### 1. Create a New Trigger

Go to the Triggers tab in Orchestrator.<br>
Click Add Trigger.<br>
Choose the process you created.<br>
Configure the execution schedule (e.g., daily, weekly, specific times).<br>
Assign the Unattended Robot to run the process.

### Step 5: Monitor the Process

Use the Jobs tab in Orchestrator to monitor the status of your processes.<br>
Logs and execution details are available in real-time.

## UiPath WorkFlow:

![alt text](<img/Screenshot 2024-10-13 132421.png>)
![alt text](<img/Screenshot 2024-10-13 132341.png>)

## Result:

The unattended robot process is successfully automated and scheduled using Orchestrator. It will run on the defined schedule without human intervention, and execution can be monitored through Orchestrator.
