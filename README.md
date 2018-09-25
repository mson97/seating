# seating
# Seating people at tables with designated seats

def factorial(number):
    i = number
    n = 1
    while i > 0:
        n = n * i
        i = i - 1
    return n
n = int(input("Enter the number of people\n"))

chairs = 0
table_number = 1
table_assignments = factorial(n)
while chairs < n:
    r = int(input("Enter the number of chairs at table %d\n" % table_number))
    chairs += r
    table_number += 1
    table_assignments = table_assignments / factorial(r)
print("The number of table assignments is %d" % table_assignments)
