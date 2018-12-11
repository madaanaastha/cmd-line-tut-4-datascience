# cmd-line-tut-4-datascience

## Handling Big-ish data on your local computer

*Disclaimer - Between the tutorial planned to execution, many of you learnt a lot or know a lot!

### Objectives
```
* Use "command line" as a data language
* Understand the many options to work with data files 
* Understand which of these approaches one can use or atleast know the right questions to ask 
```
### Getting the data across the network
```
* $ pwd
* $ cd tut_data/
* $ pwd
* $ ls -lh 
```

### Explore the data ###
```
* $ head HR_car_park.csv
* $ cat HR_car_park.csv
* $ wc -l HR_car_park.csv
```

### Do you need a DB ?
### Install sqlite3
```
* go to - https://www.sqlite.org/download.html and download the executable for sqlite3 
* Once installed, go to command prompt
* sqlite3
* .show
* .separator , 
Open your own database
* .open carpark
* 
CREATE TABLE hrcarpark(
Device” TEXT, 
DateTime” TEXT,
CarPlate ” TEXT,
ActTime TIME, 
IntervalTime TIME,
WeekNumber NUMERIC, 
DayOfWeek TEXT
);
* open a new tab for terminal
* sed -i '' 1d HR_car_park.csv
* In the sqlite3> prompt
* .import HR_car_park.csv hrcarpark
* .schema hrcarpark
* SELECT COUNT(*) FROM hrcarpark;
* SELECT count(DISTINCT(CarPlate)) FROM hrcarpark;
* 
* back to the terminal prompt
* grep '2018-08-[0-9]*' HR_car_park.csv > august_cars.csv
* wc -l august_cars.csv
* ls -lah

```


### Other useful resources 
```
* Read more - awk, sed, sort, cut, grep
* https://www.datascienceatthecommandline.com/ 
* https://datacarpentry.org/sql-socialsci/08-sqlite-command-line/index.html
* Practice practice :)
```

