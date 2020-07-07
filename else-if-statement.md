## else if statement - syntax

```javascript

const lifePhase = (age) => {
    if (age > 0 && age <= 3) {
        return 'baby'
    } else if (age >= 4 && age <= 12) {
        return 'child'
    } else if (age >= 13 && age <= 19) {
        return 'teen'
    } else if (age >= 20 && age <= 64) {
        return 'adult'
    } else if (age >= 65 && age <= 140) {
        return 'senior citizen'
    } else {
        return 'This is not a valid age'
    }
}

```
## else if statement - calculating average

Write a function, finalGrade(). It should:

* take three arguments of type number
* find the average of those three numbers
* return the letter grade (as a string) that the average corresponds to
return ‘You have entered an invalid grade.’ if any of the three grades are less than 0 or greater than 100

```javascript

const calculateAverage = (grade1, grade2, grade3) => {
    return (grade1 + grade2 + grade3) / 3;
}

const finalGrade = (grade1, grade2, grade3) => {
    if (grade1 < 0 || grade1 > 100 || grade2 < 0 || grade2 > 100 || grade3 < 0 || grade3 > 100) {
        return 'You have entered an invalid grade.'
    }

    const average = calculateAverage(grade1, grade2, grade3)

    if (average >= 0 && average <= 59) {
        return 'F'
    } else if (average >= 60 && average <= 69) {
        return 'D'
    } else if (average >= 70 && average <= 79) {
        return 'C'
    } else if (average >= 80 && average <= 89) {
        return 'B'
    } else if (average >= 90 && average <= 100) {
        return "A"
    }
