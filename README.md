# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:

## Exercise 1: Basic Directory and File Operations:

 Create a directory named "my-folder":

## COMMAND AND OUTPUT:

<img width="762" height="79" alt="1" src="https://github.com/user-attachments/assets/dd1dc1a7-a33f-40fb-bd89-5c4c842f9c45" />

 Remove the directory "my-folder":

## COMMAND AND OUTPUT:

<img width="765" height="38" alt="2" src="https://github.com/user-attachments/assets/a076757d-6720-4b39-a7f7-99cae92a175d" />


 Create the file Rose.txt:

## COMMAND AND OUTPUT:


<img width="770" height="311" alt="3" src="https://github.com/user-attachments/assets/90b2b288-fb83-4e71-a475-e5a939a9ab7c" />


 Create the file hello.txt using echo and redirection:


## COMMAND AND OUTPUT:


<img width="768" height="106" alt="4" src="https://github.com/user-attachments/assets/3cd3417e-7995-404e-9b9a-99c75004ad0c" />


 Copy the file hello.txt into the file hello1.txt:



## COMMAND AND OUTPUT:


<img width="762" height="67" alt="5" src="https://github.com/user-attachments/assets/08b820df-3382-49e6-879d-5057f9da6ef3" />


 Remove the file hello1.txt:


## COMMAND AND OUTPUT:


<img width="768" height="199" alt="6" src="https://github.com/user-attachments/assets/6dc573ec-7da5-4feb-a1b0-6d8eb47e1255" />


 List out the file hello1.txt in the current directory:


## COMMAND AND OUTPUT:

<img width="767" height="126" alt="8" src="https://github.com/user-attachments/assets/ae7c98dc-e8a7-401d-812f-c0d64a464f36" />

 List out all the associated file extensions:

## COMMAND AND OUTPUT

<img width="762" height="516" alt="7" src="https://github.com/user-attachments/assets/783c010d-cd41-4860-b6b8-8497aca32871" />

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT:

<img width="757" height="177" alt="9" src="https://github.com/user-attachments/assets/d00d8868-d71a-4fb4-90f3-bc6912c722cd" />



## Exercise 2: Advanced Batch Scripting

## Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%!
pause
```

## OUTPUT:

<img width="759" height="124" alt="10" src="https://github.com/user-attachments/assets/96ef7309-9cb2-494e-b5bf-1faae66840c6" />

## Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
1.Prompt the user to enter a number.
2.Calculate the remainder when the number is divided by 2.
3.Display whether the number is odd or not.
4.Ask the user if they want to check another number.
5.Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
6.Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause

```


## OUTPUT:

<img width="753" height="249" alt="11" src="https://github.com/user-attachments/assets/72a4378c-7f0e-4981-aa89-e0fe37b86247" />


## Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.


```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```

## OUTPUT:

<img width="769" height="218" alt="12" src="https://github.com/user-attachments/assets/7a009d9a-c965-4561-bffc-f9c4928cfae2" />


## Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
1.Use the IF EXIST conditional statement.
2.Make sure the script works for files located in the same directory as the batch file.
3.Use pause to keep the command window open after displaying the message.
4.Expected Output (if the file exists):


```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause

```


## OUTPUT:

<img width="757" height="242" alt="13" src="https://github.com/user-attachments/assets/dc145219-a00b-4ebc-aa0c-016dd745470a" />


## Write a batch script that displays a simple menu with three options:
1.Say Hello – Displays the message Hello, World!
2.Create a File – Creates a file named newfile.txt with the content This is a new file
3.Exit – Exits the script with a goodbye message
4.The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause

```

## OUTPUT

<img width="751" height="414" alt="14" src="https://github.com/user-attachments/assets/3bc84aef-6acd-47c3-900b-3567258dae4f" />


# RESULT:
The commands/batch files are executed successfully.

