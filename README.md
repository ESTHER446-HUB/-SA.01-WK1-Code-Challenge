<<<<<<< HEAD
# -SA.01-WK1-Code-Challenge
=======
# CODE CHALLENGE 

## Learnings goals
solving practical problems using 
Functions
Conditions
logic bulding


##  Challenge 1: Student Grade Generator
# Statement
Write a program that prompts the user to input student marks.  
The input should be between **0 and 100**. The output should be the correct grade:  

- **A:** 80–100  
- **B:** 60–79  
- **C:** 50–59  
- **D:** 40–49  
- **E:** less than 40  

# Explanation: 
- We check if the mark is valid (between 0 and 100).  
- We use **if...else if...else** conditions to check where the mark falls.  
- The program then outputs the correct grade.  

# Code:
```javascript
function studentGrade(marks) {
  if (marks > 100 || marks < 0) return "Invalid input";
  if (marks >= 80) return "A";
  else if (marks >= 60) return "B";
  else if (marks >= 50) return "C";
  else if (marks >= 40) return "D";
  else return "E";
}

console.log(studentGrade(85)); // A
example 
StudentGrade(80) -A





## Challenge 2: Speed Detector 
# Statement 
write a program that takes the speed of a car as input 

## Explanation 
check if the speed is <=70 then it is safe 
calculate the above 70 the driver is the divide extra by 5 to get number of demerits 
use math.floor() to ensure points are in whole numbers

function speedDetector(speed) {
  const speedLimit = 70;
  const kmPerDemerit = 5;

  if (speed <= speedLimit) {
    return "Ok";
  } else {
    const points = Math.floor((speed - speedLimit) / kmPerDemerit);
    if (points > 12) {
      return "License suspended";
    } else {
      return "Points: ${points}";
    }
  }
}

console.log(speedDetector(80)); // Points: 2

example 
speeddetector(60) ok 
speeddetector(140) license suspended

## Challenge 3 : Net Salary Calculator 



Statement:
Write a program to calculate an individual’s Net Salary by getting inputs of basic salary and benefits.
The program must calculate:

Gross Salary = basic salary + benefits

PAYE (Tax) → according to KRA tax bands

NHIF Deductions → according to NHIF rates

NSSF Deductions → 6% of pensionable pay (up to a limit)

Net Salary = Gross Salary – (PAYE + NHIF + NSSF)

Explanation:

The Gross Salary is the total of basic salary and benefits.

PAYE is calculated progressively: different percentages for different ranges.

NHIF depends on salary ranges (e.g., Ksh 150 for ≤ 5,999, up to Ksh 1,700 for >= 100,000).

NSSF is 6% of salary, capped at Ksh 18,000.

Finally, Net Salary is what remains after all deductions.

Code:
function netSalaryCalculator(basicSalary, benefits) let grossSalary = basicSalary + benefits; // PAYE let paye = 0; if (grossSalary <= 24000) { paye = grossSalary * 0.1; } else if (grossSalary <= 32333) { paye = (24000 * 0.1) + ((grossSalary - 24000) * 0.25); } else { paye = (24000 * 0.1) + (8333 * 0.25) + ((grossSalary - 32333) * 0.3); } // NHIF let nhif = grossSalary <= 5999 ? 150 : grossSalary <= 7999 ? 300 : 1200; // NSSF let nssf = Math.min(grossSalary, 18000) * 0.06; // Net Salary let netSalary = grossSalary - (paye + nhif + nssf); return { grossSalary, paye, nhif, nssf, netSalary }; } console.log(netSalaryCalculator(50000, 10000)); 
Sample Output:
{ grossSalary: 60000, paye: 14600, nhif: 1200, nssf: 1080, netSalary: 43120 } 
References:

KRA Tax Rates

NHIF Rates
>>>>>>> 8480d97 (Codechallenge)
