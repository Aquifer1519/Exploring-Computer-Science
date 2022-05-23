# Check for and adjust month input if necessary
def validateMonth(m):
    if (m<1 or m>12):
        m = 1
    return m
    
def leap_year(y):
    if (y%4 == 0 and y%100 != 0):
        return True
    elif (y%4 == 0 and y%100 == 0 and y%400 == 0):
        return True
    else: 
        return False

# Check for and adjust day input if necessary
# (don't forget about leap year)
def validateDay(m, d, y):
    if(d<1 or d>31):
        return 1
    elif(m == 2 and leap_year(y) == True):
        if (d > 29 or d<1):
            return 1
        else:
            return d
    elif(m == 2 and leap_year(y) == False):
        if(d>28 or  d<1):
            return 1
        else:
            return d
    elif (m == 4 or m ==6 or m == 9 or m == 11):
        if(d>30 or d<1):
            return 1
        else: 
            return d
    else:
        return d

# This function is used to print all events to the user in the format
# Event
# Date: Month Day, Year
def printEvents():
    for i in range(len(eventMonth)):
        if(eventMonth[i] == 1):
            eventMonth[i] = "January"
        if(eventMonth[i] == 2):
            eventMonth[i] = "February"
        if(eventMonth[i] == 3):
            eventMonth[i] = "March"
        if(eventMonth[i] == 4):
            eventMonth[i] = "April"
        if(eventMonth[i] == 5):
            eventMonth[i] = "May"
        if(eventMonth[i] == 6):
            eventMonth[i] = "June"
        if(eventMonth[i] == 7):
            eventMonth[i] = "July"
        if(eventMonth[i] == 8):
            eventMonth[i] = "August"
        if(eventMonth[i] == 9):
            eventMonth[i] = "September"
        if(eventMonth[i] == 10):
            eventMonth[i] = "October"
        if(eventMonth[i] == 11):
            eventMonth[i] = "November"
        if(eventMonth[i] == 12):
            eventMonth[i] = "December"
    
    for i in range(len(eventName)):
        print(eventName[i])
        print("Date: " + eventMonth[i] + " " + str(eventDay[i]) + ", " + str(eventYear[i]))


# This function is used to prompt, adjust and 
# append values to the 4 parallel arrays
def addEvent():
    name = input("What is the event: ")
    month = int(input("What is the month (number): "))
    day = int(input("What is the date: "))
    year = int(input("What is the year: "))
    month = validateMonth(month)
    day = validateDay(month, day, year)
    eventName.append(name)
    eventMonth.append(month)
    eventDay.append(day)
    eventYear.append(year)

    
#*********** MAIN **********
eventName = []
eventMonth = []
eventDay = []
eventYear = []

addEvent()

again = input("Do you want to enter another event? NO to stop: ")
while(again != "NO"):
    addEvent()
    again = input("Do you want to enter another event? NO to stop: ")
print("******************** List of Events ********************")
printEvents()
