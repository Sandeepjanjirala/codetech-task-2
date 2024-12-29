# Simple Student Grades Management Program

def calculate_gpa(average):
    if average >= 90:
        return 'A', 10
    elif average >= 80:
        return 'B', 8.0
    elif average >= 70:
        return 'C', 6.0
    elif average >= 60:
        return 'D', 4.0
    else:
        return 'F', 2.0

# Main program
grades = []

num_subjects = int(input("Enter the number of subjects: "))
for _ in range(num_subjects):
    grade = float(input("Enter the grade: "))
    grades.append(grade)

average = sum(grades) / num_subjects
letter_grade, gpa = calculate_gpa(average)

print(f"\nAverage Grade: {average:.2f}")
print(f"Letter Grade: {letter_grade}")
print(f"GPA: {gpa:.2f}")
