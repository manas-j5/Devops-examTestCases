KIET_DevOps_DebugChallenge
DevOps Exam — Test Cases
KIET Group of Institutions | Even Sem 2026
Instructions: Read each test case carefully. Complete all tasks in sequence. Show your terminal output / screenshots as proof of completion wherever mentioned.

Test Case 1 — Linux System Audit & User Management
Scenario: You are a Linux system administrator onboarding new employees at a tech company. Complete the following tasks on your system.

Tasks
Check the identity of the currently logged-in user and display the username of the current session.

Check which users are currently logged into the system and what they are doing.

View the login history of the system.

Display complete system information, the hostname, and how long the system has been running.

Create two groups: developers and qa. Verify both groups were successfully created and display the complete list of groups on the system.

Create the following users and assign each to their respective group:

Employee	Department
aman	developers
ritu	developers
karan	qa
Employee ritu has resigned. Ensure she has no active sessions, delete her account along with her home directory, and verify she no longer exists on the system.

Expected Outcome
System audit commands display current user, active sessions, login history, hostname, and uptime without errors.
Groups developers and qa appear in the system group list.
Users aman and karan are created and assigned to the correct groups (verified via id command).
After deletion, any attempt to look up ritu returns: "no such user".
Test Case 2 — File Permission Configuration
Scenario: A web server requires a properly configured index.html file with specific ownership and access permissions.

Tasks
Navigate to your home directory and create a file named index.html.
Add any HTML text content to the file.
Check the file's current default permissions.
Grant full permissions (read, write, execute) to all users on the file.
Change the file owner and group to www-data.
Change the file permissions to 755.
Display the final permissions and ownership to verify the configuration.
Expected Outcome
File index.html exists in the home directory with content.
After step 4, permissions show rwxrwxrwx.
After step 5, owner and group both show www-data.
Final ls -l output shows:
-rwxr-xr-x 1 www-data www-data ... index.html
Test Case 3 — Node.js Application Setup & Git Integration
Scenario: You are setting up a new Node.js REST API from scratch and publishing it to GitHub.

Tasks
Initialize a new Node.js project and install the required dependencies: express and @types/express (as a dev dependency).
Create an index.js file that starts an Express server on port 8080 with the following endpoint:
GET /health — returns HTTP status 200 with the JSON response { "status": "OK" }.
Initialize a Git repository in the project folder.
Create an initial commit with all project files.
Create a GitHub repository named nodejs-api and push your code to it.
Expected Outcome
Project folder contains package.json, node_modules/, and index.js.
Running the server locally and calling GET /health returns:
{ "status": "OK" }
GitHub repository nodejs-api is publicly visible with at least one commit containing all project files.


GitHub repository nodejs-api is publicly visible with at least one commit containing all project files
🌐 Repository Link

https://github.com/manas-j5/nodejs-api
