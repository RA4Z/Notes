Is a [[Packages|Module]] in Python that provides classes for manipulating dates and times. Supporting arithmetic operations, attribute extraction and output formatting.

## Examples of use

#### 1. datetime.date
Represents a date (year,month and day)
```Python
from datetime import date
# Create a date object
d = date(2023, 10, 5)
# Access year, month, and day
print(d.year) # 2023
print(d.month) # 10
print(d.day) # 5
```

#### 2. datetime.time
Represents a time, independent of any particular day, assuming every day has exactly 246060 seconds
```Python
from datetime import time
# Create a time object
t = time(14, 30, 45)
# Access hour, minute, and second
print(t.hour) # 14
print(t.minute) # 30
print(t.second) # 45
```

#### 3. datetime.datetime
A combination of a date and a time. It includes attributes for year, month, day, hour, minute, second, microsecond, and tzinfo
```Python
from datetime import datetime
# Create a datetime object
dt = datetime(2023, 10, 5, 14, 30, 45)
# Access date and time components
print(dt.year) # 2023
print(dt.month) # 10
print(dt.day) # 5
print(dt.hour) # 14
print(dt.minute) # 30
print(dt.second) # 45
print(dt.microsecond)# 0
```

#### 4. datetime.timedelta
Represents a duration, the difference between two datetime or date instances
```Python
from datetime import timedelta
# Create a timedelta object
delta = timedelta(days=5, hours=3, minutes=30)
# Access days, seconds, and microseconds
print(delta.days) # 5
print(delta.seconds) # 12600 (3 hours and 30 minutes in seconds)
print(delta.microseconds) # 0
```