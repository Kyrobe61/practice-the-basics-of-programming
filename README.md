# practice-the-basics-of-programming
measuring how long it takes for the sound waves to bounce back

Introduction									
The aim of this assignment is to practice the basics of programming. You will get some inputs from the user, do some arithmetic operations and display the output to the user.

Description

The Photoacoustic Airborne Sonar System (PASS) is a drone attachment designed for underwater reconnaissance. It is like a special tool that helps us "see" things underwater using sound. This device works by sending out sound waves from an aircraft towards the water below. When these sound waves hit objects underwater, like fish or rocks, they bounce back to the aircraft. Sensors on the aircraft then listen for these bouncing sound waves. By measuring how long it takes for the sound waves to bounce back we can calculate the distance between the aircraft and the object.

Now, you are among the pioneers exploring the lives of new planets, where teams of scientists and engineers operate Photoacoustic Airborne Sonar Systems (PASS). Your task is to write a simple Python code to calculate the time it takes for a sound wave to travel to an object, reflect off it, and return as an echo.

 

The speed of sound varies between gasses and liquids. In our scenario, as we investigate underwater objects using sound waves emitted from an aircraft, the sound wave will travel through both gas and liquid environments as it can be seen from the figure. For simplicity, we will be setting the speed of sound in air as 343 meters per second. 

To calculate the speed of the sound in liquids, you will need to use the formula given below, where K_s is bulk modulus of the liquid (Pa), ρ is density (kg/m^3 ), and c is the speed of sound in liquids (m/s).
c=√(K_s/ρ)


You are going to get the following information from the user:

	- Bulk modulus of the liquid (in GPa): Required to calculate the speed of sound in liquids.
	- Density: Required to calculate the speed of sound in liquids.
	- Measured distance: The distance (in terms of meters) between the aircraft and the object.
	- Altitude: The distance (in terms of meters) between the drone and the surface.

After obtaining the inputs from the user, you need to calculate the speed of the sound in the liquid using the provided formula. However, remember that the bulk modulus is provided in GPa, but the formula requires it in Pa. Therefore, we need to convert the units, where 1 GPa = 10^9Pa. Once you convert the units, you can calculate the speed of the sound in the liquid.

Since we know the speed of the sound in both air and liquid, as well as the altitude of the aircraft and the distance between the aircraft and the object, we can calculate the time it takes for a sound wave to travel to an object, reflect off it, and return as an echo. 

In total, there are four sections that a sound wave needs to travel through.

	The first section is when a sound wave is initially emitted from an aircraft and travels through the air until it reaches the liquid. To calculate the time spent, we need to divide the “altitude” by the speed of sound in air.

	The second section is when a sound wave enters the liquid and travels until it reaches the object. To calculate the time spent, we first need to find the distance between the object and the surface of the liquid. This can be easily found by subtracting the "measured distance" from the "altitude". After finding the distance, we divide it by the speed of sound in the liquid to calculate the time spent.

	The third and fourth sections represent the echo phases where the sound wave reflects from the object and returns all the way back to the aircraft. Consequently, the time spent in these sections is equal to the time spent in sections one and two. Therefore, we can multiply the sum of sections one and two to find the total time spent.

Output
Your program needs to calculate and display the calculated speed of sound in air with exactly two decimal places (see sample runs). In addition, you also need to print the total time it takes for a sound wave to travel to an object, reflect off it, and return as an echo.
The output of your program should be exactly in the following format:

h hour(s), m minute(s) and s second(s), ms millisecond(s).

Your program should calculate four numbers (h, m, s, and ms) for its output. If one of these results is 0, your program should also print that. 
Please note that h, m and s values must be displayed as integers (without any precision), and the ms value must be displayed as a real number with exactly four decimal places (Hint: use format function that was explained in the recitation materials). 
Note: 1s = 10^3ms
You may check the "Sample Runs" section given below for some examples.





Sample Runs
Below, we provide some sample runs of the program that you will develop. The italic and bold phrases are inputs taken from the user. You have to display the required information in the same order and with the same words and characters as below. 

Sample Run 1
Enter the bulk modulus of the liquid (in GPa): 2.2
Enter the density of the liquid (in kg/m^3): 1030
Enter the measured distance between object and drone: 10000
Enter the altitude of the drone: 7000

Calculated speed of sound in liquid is: 1461.48 m/sec.
0 hour(s), 0 minute(s), 44 second(s), 921.7553 millisecond(s).

Sample Run 2
Enter the bulk modulus of the liquid (in GPa): 1.06
Enter the density of the liquid (in kg/m^3): 789
Enter the measured distance between object and drone: 35000
Enter the altitude of the drone: 34000

Calculated speed of sound in liquid is: 1159.08 m/sec.
0 hour(s), 3 minute(s), 19 second(s), 976.2313 millisecond(s).

Sample Run 3
Enter the bulk modulus of the liquid (in GPa): 28.5
Enter the density of the liquid (in kg/m^3): 631
Enter the measured distance between object and drone: 3360.297700191818
Enter the altitude of the drone: 0

Calculated speed of sound in liquid is: 6720.60 m/sec.
0 hour(s), 0 minute(s), 1 second(s), 0.0000 millisecond(s).


Sample Run 4
Enter the bulk modulus of the liquid (in GPa): 0.2
Enter the density of the liquid (in kg/m^3): 1340
Enter the measured distance between object and drone: 890000
Enter the altitude of the drone: 786430

Calculated speed of sound in liquid is: 386.33 m/sec.
1 hour(s), 25 minute(s), 21 second(s), 766.2636 millisecond(s).
