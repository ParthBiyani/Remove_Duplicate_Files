@echo off
setlocal enabledelayedexpansion

REM Set the target folder where you want to search for files
set "target_folder=C:\Users\Asus\Desktop\Test"

REM Set the string you want to search for in file names
set "search_string=202326-202326"

REM Recursively search for files containing the specified string
for /r "%target_folder%" %%F in (*%search_string%*) do (
    echo Deleting: "%%F"
    del "%%F"
)

echo All files containing "%search_string%" have been deleted.
pause
