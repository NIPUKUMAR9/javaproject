# CCRM Usage

## Build
- PowerShell
```
mkdir out
javac -d out -encoding UTF-8 $(Get-ChildItem -Recurse src\main\java\*.java | ForEach-Object { $_.FullName })
```

## Run
```
java -cp out edu.ccrm.cli.Main
```

## Enable assertions
```
java -ea -cp out edu.ccrm.cli.Main
```

## Sample data
- Import students: test-data/students.csv
- Import courses: test-data/courses.csv

CSV format (header optional):
- students.csv: regNo,fullName,email,active
- courses.csv: code,title,credits,department,semester
