# Scheduler
A simple scheduler, CLI based.

## Requirements
- Pandas ( for sorting )
- TinyDB ( for storing data )
- win10toast ( for notification )

## Scheduler Usage
Run the program in terminal and it will loop every one minute to check if there exist a schedule at that exact time.

## Scheduler Functions
### insert
Insert a schedule into the program, you can't input a schedule at the same date and time. <br>
The repeat argument is still in development and has no effect.
```python
insert(title, date, time, end, repeat='no')
# All arguments are STRING.
# date format ddmmyyyy
# time and end format hhmm
```
### remove
Remove a schedule from the database.
```python
remove(date, time)
# All arguments are STRING.
# date and time format is the same.
```
### checktime
Checks if there exist a schedule at current time ( this could be modified to notify e.g 15 minutes before the schedule)
```python
checktime()
# returns if there exist. If it's empty that means there's no schedule.
```
### schedules
List out all the schedules 
```python
schedules()
# return a sorted pandas dataframe
```
