// 1. Student Object
const student = {
    name: "Umesh",
    age: 21,
    course: "Information Technology",
    marks: 450
};

// 2. Arrow Function
const calculatePercentage = (marks) => (marks / 500) * 100;

// 3. Template Literals
console.log(`Student Name: ${student.name}`);
console.log(`Course: ${student.course}`);

// 4. Destructuring
const { name, age, marks } = student;

console.log(`Age: ${age}`);
console.log(`Marks: ${marks}`);

const subjects = ["HTML", "CSS", "JavaScript"];
const [s1, s2, s3] = subjects;

console.log(`Subjects: ${s1}, ${s2}, ${s3}`);

// 5. Spread Operator
const additionalInfo = {
    city: "Pune",
    college: "Indira College"
};

const finalStudent = {
    ...student,
    ...additionalInfo,
    percentage: calculatePercentage(marks)
};

console.log(`Percentage: ${finalStudent.percentage}%`);
console.log(`City: ${finalStudent.city}`);
console.log(`College: ${finalStudent.college}`);

// 6. Rest Operator
const calculateTotal = (...numbers) => {
    return numbers.reduce((total, n) => total + n, 0);
};

console.log(`Total Marks: ${calculateTotal(80, 90, 85)}`);

// 7. Promise
const checkResult = () => {
    return new Promise((resolve, reject) => {
        console.log("Checking result...");

        setTimeout(() => {
            let passed = true;

            if (passed) {
                resolve("Student has passed the exam.");
            } else {
                reject("Student has failed the exam.");
            }
        }, 2000);
    });
};

// 8. Async/Await
async function displayResult() {
    try {
        const message = await checkResult();
        console.log(message);
        console.log("Result displayed successfully.");
    } catch (error) {
        console.log(error);
    }
}

displayResult();
