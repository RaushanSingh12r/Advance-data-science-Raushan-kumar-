
print("=" * 50)
print("   HOSPITAL APPOINTMENT & DEPARTMENT MANAGEMENT SYSTEM")
print("=" * 50)

patient_name = input("Enter patient name: ")

requested_input = input("Enter requested departments: ")
visited_input = input("Enter previously visited departments: ")
doctor_input = input("Enter preferred doctors: ")


requested_list = requested_input.split(",")
visited_list = visited_input.split(",")
doctor_list = doctor_input.split(",")

requested_list = [x.strip().title() for x in requested_list]
visited_list = [x.strip().title() for x in visited_list]
doctor_list = [x.strip().title() for x in doctor_list]


available_departments = {"Cardiology","Neurology","Orthopedics","Dermatology","Pediatrics","General Medicine"}

emergency_departments = {"Cardiology","Neurology","Emergency Medicine"}

available_doctors = {"Dr.Rahul","Dr.Kumar","Dr.Aditya","Dr.Raushan","Dr.singh"}


requested = set(requested_list)
visited = set(visited_list)
doctors = set(doctor_list)


available = requested & available_departments

unavailable = requested - available_departments

common = requested & visited

emergency = requested & emergency_departments

available_doctors_list = doctors & available_doctors

duplicates = []

for x in requested_list:
    if requested_list.count(x) > 1 and x not in duplicates:
        duplicates.append(x)

# Appointment decision
if emergency:
    recommended = list(emergency)[0]
    status = "Emergency Appointment"

elif available:
    recommended = list(available)[0]
    status = "Appointment Available"

else:
    recommended = "None"
    status = "Appointment Not Available"

print("\n")
print("=" * 50)
print("                FINAL APPOINTMENT REPORT")
print("=" * 50)

print("Patient Name              :", patient_name)

print("\nRequested Departments     :", sorted(requested))

print("Available Departments     :", sorted(available))

print("Unavailable Departments  :", sorted(unavailable))

print("Common Departments        :", sorted(common))

print("Previously Visited        :", sorted(visited))

print("Emergency Departments     :", sorted(emergency))

print("Duplicate Requests        :", duplicates)

print("Preferred Doctors         :", sorted(doctors))

print("Available Preferred Docs  :", sorted(available_doctors_list))

print("Recommended Department   :", recommended_department)

print("Final Appointment Status  :", appointment_status)

print("=" * 50)


print("\nMembership Checking:")

check_department = input(
    "Enter a department to check availability: "
)

check_department = check_department.strip().title()


if check_department in available_departments:

    print(check_department, "is available in the hospital.")

else:

    print(check_department, "is NOT available in the hospital.")


print("\nThank you for using the Hospital Appointment System.")
