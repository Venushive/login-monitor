LoginMonitor Program 

It’s a Python program for checking login records. It turns each line into a record, then shows failed logins by user, the most suspicious IP, any locked accounts, the IPs each user connected from, and the busiest hour. It ends with a short list of security warnings based on what it found.







Running the Program

You need Python 3, but no extra libraries. 

Run: python assignment_starter_login_monitor.py

It uses the sample raw_logs from the top of the file and prints a summary, then a test block for each method.








busiest_hour() - how it works

In busiest_hour(), each timestamp is a string, such as "2026-10-10 08:15:02". I split the timestamp at the space, then take the first two characters of the time part to get the hour, like "08". I keep a count for each hour in a dictionary, using .get(hour, 0) + 1 so the count increases for every login, whether it succeeded or failed. Then I use max() with the count as the key to find the hour with the most logins. The function returns that hour and its count as a tuple, or None if there are no records.
