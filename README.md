# Application-of-Python-in-the-field-of-Soil-Mechanics
ASSIGNMENT NO. 06

Q.1) # Stress when depth is constant

# Input values
Q = float(input("Enter the value of load in kN: "))
N = int(input("Number of data values of radial distance: "))  pi = 3.14159265359
Z = float(input("Depth (m): "))  

r = []
for i in range(1, N + 1):
    Value_r = float(input(f"Enter radial distance {i} in m: "))      r.append(Value_r)

# Calculate stress for each radial distance
for radial_distance in r:
    Stress = ((3 * Q) / (2 * pi * Z * Z)) * (((1 / (1 + ((radial_distance / Z) ** 2))) ** 2.5))
    print(f"Stress at radial distance {radial_distance} m: {Stress:.2f} kN/m^2")  

OUTPUT:
Enter the value of load in kN: 2500
Number of data values of radial distance: 5
Depth (m): 6
Enter radial distance 1 in m: 2
Enter radial distance 2 in m: 3
Enter radial distance 3 in m: 4
Enter radial distance 4 in m: 5
Enter radial distance 5 in m: 6
Stress at radial distance 2.0 m: 25.48 kN/m^2
Stress at radial distance 3.0 m: 18.98 kN/m^2
Stress at radial distance 4.0 m: 13.22 kN/m^2
Stress at radial distance 5.0 m: 8.87 kN/m^2
Stress at radial distance 6.0 m: 5.86 kN/m^2


Q.2)    # Stress when radius is constant

# Input values
Q = float(input("Enter the value of load in kN: "))
M = int(input("Number of data values of depth: "))
pi = 3.14159265359
r = float(input("Radial Distance (m): "))  # Added unit for clarity
Z = []

# Collecting depth values
for j in range(1, M + 1):
    Value_Z = float(input(f"Enter depth {j} in m: "))  # Formatted for clarity
    Z.append(Value_Z)

# Calculate stress for each depth value
for Value_Z in Z:
    Stress = ((3 * Q) / (2 * pi * Value_Z * Value_Z)) * (((1 / (1 + ((r / Value_Z) ** 2))) ** 2.5))
    print(f"Stress at depth {Value_Z} m: {Stress:.2f} kN/m^2")  # Formatted output

OUTPUT:
Enter the value of load in kN: 2500
Number of data values of depth: 6
Radial Distance (m): 5
Enter depth 1 in m: 1
Enter depth 2 in m: 2
Enter depth 3 in m: 3
Enter depth 4 in m: 4
Enter depth 5 in m: 5
Enter depth 6 in m: 6
Stress at depth 1.0 m: 0.35 kN/m^2
Stress at depth 2.0 m: 2.11 kN/m^2
Stress at depth 3.0 m: 4.78 kN/m^2
Stress at depth 4.0 m: 7.10 kN/m^2
Stress at depth 5.0 m: 8.44 kN/m^2
Stress at depth 6.0 m: 8.87 kN/m^2

Q.3) # Calculating the stress by Boussineq's Theory
Q = float(input("Enter the value of given load (kN): "))  # Load in kN
z = float(input("Enter the distance of vertical stress (m): "))  # Depth in meters
r = float(input("Enter the distance of horizontal stress (m): "))  # Radial distance in meters

# Boussineq's equation
stress = (3 * Q * (1 / (1 + (r / z) ** 2))) / (2 * 3.14 * (z ** 2))

# Print the result
print("The value of stress is:", stress, "kN/m^2")  # Stress in kN/m^2

OUTPUT:
Enter the value of given load (kN): 2500
Enter the distance of vertical stress (m): 6
Enter the distance of horizontal stress (m): 5
The value of stress is: 19.578155998746993 kN/m^2
