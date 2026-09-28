# 🌾 AgroVision: Smart Agriculture Insights Platform

### Turning agricultural inputs into actionable insights for farmers.

**A data-driven platform that combines a web interface with backend data processing. This repository contains its Java backend building blocks: 31 tested programs for input, calculation, decision logic, and output.**

☕ **Java 8+** &nbsp;|&nbsp; 📄 &nbsp;|&nbsp; 📏  &nbsp;|&nbsp; 

---

## 📌 Problem Statement

Farming decisions depend on information, but that information is often raw, scattered, or hard to interpret. Turning agricultural inputs into clear guidance usually needs technical knowledge or expert help, so decisions end up based on guesswork instead of evidence.

**AgroVision** closes this gap. It takes inputs, processes them in the backend, and produces results a farmer can act on. This repository holds the Java logic that does the processing.

---

## 🎯 Unique Selling Proposition

> *"AgroVision turns raw inputs into clear, actionable results with small, single-purpose backend modules that are easy to read, test, and extend."*

---

## ✨ Key Features

| Feature | Description | Example in the code |
|---------|-------------|---------------------|
| ⌨️ **Interactive Input** | 19 programs read live values from the user with `Scanner` | `EmployeeDetails`, `ArithmeticOperations`, `GradeStudent` |
| 🧮 **Calculation Engine** | Arithmetic, compound, bitwise, shift, and ternary operators | `ArithmeticOperations`, `ShiftOperators` |
| 🛡️ **Safe Division** | Guards against division and modulus by zero | `ArithmeticOperations`, `BasicCalculator` |
| 🔀 **Decision Logic** | `if / else if / else` rules for grading, results, and comparisons | `GradeStudent`, `ExamResult`, `DayName` |
| 🔁 **Repetition** | `for` loops and a `do-while` input loop | `MultiplicationTable`, `sumofsquares`, `AcceptUntilZero` |
| 🗃️ **Record Handling** | Collects and prints a full record with mixed data types | `EmployeeDetails` |
| 🔄 **Type Conversion** | Boxing and unboxing of `Integer`, `Double`, and `Character` | `BoxingDemo`, `AutoUnboxingDemo` |
| 📅 **Date and Time** | Reads day, week, and time fields with `Calendar` | `calendar` |

---

## 🏗️ Solution Architecture

Every program in the backend follows the same three-stage pattern:

```
┌──────────────────────────────────────────────────────┐
│                  FARMER / USER INPUT                  │
└──────────────────────────┬───────────────────────────┘
                           │
             ┌─────────────▼─────────────┐
             │        INPUT STAGE        │
             │   Scanner reads numbers,  │
             │   text, and booleans      │
             └─────────────┬─────────────┘
                           │
             ┌─────────────▼─────────────┐
             │      PROCESSING STAGE     │
             │  Operators | Conditions   │
             │  Loops | Type conversion  │
             └─────────────┬─────────────┘
                           │
             ┌─────────────▼─────────────┐
             │       OUTPUT STAGE        │
             │  Clear, labeled results   │
             │  printed to the console   │
             └───────────────────────────┘
```

---

## 🧭 Program Flow

```
User runs a program
    └─► Enters values              (Scanner input)
            └─► Program validates and processes   (operators, conditions, loops)
                    └─► Result is printed         (grade, total, comparison, record)
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Language | Java 8+ |
| User Input | `java.util.Scanner` |
| Date and Time | `java.util.Calendar`, `java.util.Date` |
| Type Wrappers | `Integer`, `Double`, `Character` |
| Code Organization | Java packages: `myproject` (29 programs), `strings` (2 programs) |
| Build | `javac` (JDK) |
| Version Control | Git and GitHub |

---

## 🚀 Getting Started

### Prerequisites

- **Java JDK 8 or higher** ([download](https://www.oracle.com/java/technologies/downloads/))
- Git
- A terminal, or an IDE such as IntelliJ IDEA, Eclipse, or VS Code

Check that Java is installed:

```bash
java -version
javac -version
```

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/sabbir151-eng/agrovision_app.git
cd agrovision_app

# 2. Compile all programs into an "out" folder
mkdir out
javac -d out *.java

# 3. Run any program using its package name
java -cp out myproject.EmployeeDetails
```

### Running Other Programs

```bash
java -cp out myproject.GradeStudent
java -cp out myproject.ArithmeticOperations
java -cp out strings.ReadAndPrintString
```

| Package | Programs |
|---------|----------|
| `strings` | `DisplayStringObject`, `ReadAndPrintString` |
| `myproject` | All the other 29 programs |

> 💡 **Using an IDE?** Create a Java project, place the files under `src/myproject/` (and the two `strings` programs under `src/strings/`), then run any file's `main` method.

---

## 📦 Program Index

The **Input** column shows whether a program reads live values (⌨️) or uses fixed values built into the code (📌).

### 🔢 Data Types and Type Conversion

| File | What it does | Input |
|------|--------------|:-----:|
| `SimpleDataTypes.java` | Declares and prints `byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`, and `String` | 📌 |
| `autocast.java` | Reads an `int` and assigns it to another `int` variable | ⌨️ |
| `BoxingDemo.java` | Manual boxing with `Integer.valueOf()`, `Character.valueOf()`, `Double.valueOf()` | 📌 |
| `UnboxingDemo.java` | Manual unboxing from `Integer`, `Double`, `Character` back to primitives | 📌 |
| `AutoBoxingDemo.java` | Automatic boxing of `int`, `char`, and `double` | 📌 |
| `AutoUnboxingDemo.java` | Automatic unboxing of `Integer`, `Double`, and `Character` | 📌 |

### ➕ Operators and Calculation

| File | What it does | Input |
|------|--------------|:-----:|
| `ArithmeticOperations.java` | Prints sum, difference, product, division, and modulus, with a division-by-zero check | ⌨️ |
| `CompoundAssignment.java` | Applies `+=`, `-=`, `*=`, `/=`, `%=` step by step, starting from 10 | 📌 |
| `IncrementDecrementDemo.java` | Shows the effect of `a++`, `++a`, `a--`, and `--a` starting from 5 | 📌 |
| `BitwiseOperators.java` | Prints the results of `&`, `\|`, `^`, and `~` for 5 and 3 | 📌 |
| `ShiftOperators.java` | Reads a number and shift amount, then prints left shift (`<<`) and right shift (`>>`) | ⌨️ |
| `TernaryGreater.java` | Reads two numbers and finds the greater one with the ternary operator | ⌨️ |
| `GreaterNumber.java` | Finds the greater of two fixed values (30 and 50) with the ternary operator | 📌 |

### 🔀 Decision Logic

| File | What it does | Input |
|------|--------------|:-----:|
| `EvenOddCheck.java` | Tells whether a number is even or odd | ⌨️ |
| `PositiveCheck.java` | Tells whether a number is positive | ⌨️ |
| `CompareIntegers.java` | Compares two integers: greater, smaller, or equal | ⌨️ |
| `gratersnymber.java` | Compares three numbers using `if / else if / else` | ⌨️ |
| `DayName.java` | Converts a day number (1 to 7) to a day name, where 1 is Sunday | ⌨️ |
| `GradeStudent.java` | Converts marks to a grade: A (90+), B (80+), C (70+), D (60+), E (40+), F (below 40) | ⌨️ |
| `ExamResult.java` | Passes a student only if both theory and practical scores are 50 or above | ⌨️ |

### 🔁 Loops and Repetition

| File | What it does | Input |
|------|--------------|:-----:|
| `PrintNumbers.java` | Prints the numbers from 1 to N | ⌨️ |
| `MultiplicationTable.java` | Prints the multiplication table (1 to 10) of a number | ⌨️ |
| `sumofsquares.java` | Calculates 1² + 2² + ... + n² | ⌨️ |
| `AcceptUntilZero.java` | Keeps asking for numbers with a `do-while` loop until 0 is entered | ⌨️ |

### 📥 Input, Arrays and Strings

| File | What it does | Input |
|------|--------------|:-----:|
| `ReadAndPrint.java` | Reads 5 integers into an array and prints them | ⌨️ |
| `StaticValuesPrinter.java` | Prints the values of a static array (10, 20, 30, 40, 50) | 📌 |
| `ReadAndPrintString.java` | Reads a line of text and prints it back | ⌨️ |
| `DisplayStringObject.java` | Creates and prints a `String` object | 📌 |

### 🧩 Mini Programs

| File | What it does | Input |
|------|--------------|:-----:|
| `BasicCalculator.java` | A simple calculator: add, subtract, multiply, divide, modulus | ⌨️ |
| `EmployeeDetails.java` | Reads an ID, name, department, experience, salary, contact number, and full-time status, then prints a summary | ⌨️ |
| `calendar.java` | Uses `Calendar` and `Date` to print day of week, day of year, week of month, and time fields | 📌 |

---

## 📁 Project Structure

```
agrovision_app/
├── AcceptUntilZero.java          # do-while loop until 0 is entered
├── ArithmeticOperations.java     # + - * / % with zero-division check
├── AutoBoxingDemo.java           # automatic boxing
├── AutoUnboxingDemo.java         # automatic unboxing
├── BasicCalculator.java          # two-number calculator
├── BitwiseOperators.java         # & | ^ ~
├── BoxingDemo.java               # manual boxing with valueOf()
├── CompareIntegers.java          # greater / smaller / equal
├── CompoundAssignment.java       # += -= *= /= %=
├── DayName.java                  # day number to day name
├── DisplayStringObject.java      # String object (package: strings)
├── EmployeeDetails.java          # record input and summary
├── EvenOddCheck.java             # even or odd
├── ExamResult.java               # theory + practical pass check
├── GradeStudent.java             # marks to grade
├── GreaterNumber.java            # ternary on fixed values
├── IncrementDecrementDemo.java   # ++ and --
├── MultiplicationTable.java      # table of 1 to 10
├── PositiveCheck.java            # positive number check
├── PrintNumbers.java             # print 1 to N
├── ReadAndPrint.java             # read 5 ints into an array
├── ReadAndPrintString.java       # read a string (package: strings)
├── ShiftOperators.java           # << and >>
├── SimpleDataTypes.java          # all primitive types
├── StaticValuesPrinter.java      # static array printing
├── TernaryGreater.java           # ternary on user input
├── UnboxingDemo.java             # manual unboxing
├── autocast.java                 # int assignment
├── calendar.java                 # Calendar and Date fields
├── gratersnymber.java            # compares three numbers
├── sumofsquares.java             # 1² + 2² + ... + n²
└── README.md
```

---

## 🖥️ Sample Output

**`EmployeeDetails`**
```
Enter the employee ID: 101
Enter the employee name: Ravi Kumar
Enter the employee department: Agronomy
Enter the employee experience (in years): 5
Enter the employee salary: 45000
Enter the employee contact number: 9876543210
Is the employee full-time? (true/false): true

 Employee Details : - 
ID: 101
Name: Ravi Kumar
Department: Agronomy
Experience: 5 years
Salary: 45000
Contact Number: 9876543210
Full Time Worker: Yes
```

**`ArithmeticOperations`**
```
Enter first number: 10
Enter second number: 4
Addition: 14.0
Subtraction: 6.0
Multiplication: 40.0
Division: 2.5
Modulus: 2.0
```

**`GradeStudent`**
```
Enter marks: 85
Grade: B
```

**`ExamResult`**
```
Enter theory exam score: 60
Enter practical exam score: 45
Student did not pass both exams.
```

**`DayName`**
```
Enter day number (1-7): 3
Tuesday
```

**`CompoundAssignment`**
```
After += 5: 15
After -= 3: 12
After *= 2: 24
After /= 4: 6
After %= 3: 0
```

**`MultiplicationTable`**
```
Enter a number: 5
5 x 1 = 5
5 x 2 = 10
...
5 x 10 = 50
```

---

## 🩺 Troubleshooting

| Problem | Fix |
|---------|-----|
| `Error: Could not find or load main class EvenOddCheck` | Run it with its package: `java -cp out myproject.EvenOddCheck` |
| `'javac' is not recognized` or `command not found` | Install the JDK (not just the JRE) and add it to your `PATH` |
| `InputMismatchException` | The program expected a number. Enter a valid number when prompted |
| Program seems to hang | It is waiting for input. Type a value and press Enter |

---

## 🎓 Suggested Learning Path

1. **Basics:** `SimpleDataTypes` → `ReadAndPrintString` → `ArithmeticOperations`
2. **Operators:** `CompoundAssignment` → `IncrementDecrementDemo` → `BitwiseOperators` → `ShiftOperators` → `TernaryGreater`
3. **Decisions:** `EvenOddCheck` → `CompareIntegers` → `DayName` → `GradeStudent` → `ExamResult`
4. **Loops:** `PrintNumbers` → `MultiplicationTable` → `sumofsquares` → `AcceptUntilZero`
5. **Type conversion:** `BoxingDemo` → `UnboxingDemo` → `AutoBoxingDemo` → `AutoUnboxingDemo`
6. **Put it together:** `BasicCalculator` → `EmployeeDetails` → `calendar`

---

## 🔮 Roadmap

- [ ] Connect the backend processing to the web interface
- [ ] Expand the range of agricultural inputs the platform accepts
- [ ] Add more types of farmer-focused insights
- [ ] Add multi-language support for regional farmers
- [ ] Organize the backend code into topic-wise folders

---

## 📊 Repository Highlights

| Metric | Value |
|--------|-------|
| 📄 Programs | 31 |
| 📏 Lines of code | 660 |
| ⌨️ Interactive programs (read live input) | 19 |
| 📌 Fixed-value demo programs | 12 |
| 📦 Java packages | 2: `myproject` (29 programs), `strings` (2 programs) |
| 🗂️ Logic categories | 6 |
| ⚙️ Build | All 31 files compile together with a standard JDK |

---

## 👥 Team

Built with ❤️ for farmers.

| Role | Name |
|------|------|
| Developer | Sk Abdul Sabbir |

B.Tech in Computer Science and Engineering, Koneru Lakshmaiah Education Foundation (KLU), Hyderabad

🔗 GitHub: [@sabbir151-eng](https://github.com/sabbir151-eng)

---

## 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

**AgroVision**: *from agricultural inputs to actionable insights.*

⭐ If this project helped you, please give it a star!
