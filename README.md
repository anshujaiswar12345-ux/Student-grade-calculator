
print("===== Student Grade Calculator =====")

name = input("Enter student name: ")

marks = []
for i in range(1, 6):
    mark = float(input(f"Enter marks for Subject {i} (0-100): "))
    if mark < 0 or mark > 100:
        print("Invalid marks! Enter marks from 0 to 100.")
        exit()
    marks.append(mark)

total = sum(marks)
percentage = total / 5

if any(mark < 35 for mark in marks):
    grade = "F"
    result = "Fail"
elif percentage >= 90:
    grade = "A+"
    result = "Pass"
elif percentage >= 80:
    grade = "A"
    result = "Pass"
elif percentage >= 70:
    grade = "B"
    result = "Pass"
elif percentage >= 60:
    grade = "C"
    result = "Pass"
elif percentage >= 35:
    grade = "D"
    result = "Pass"

print("\n===== Student Result =====")
print("Name:", name)
print("Total Marks:", total, "/ 500")
print("Percentage:", round(percentage, 2), "%")
print("Grade:", grade)
print("Result:", result)
