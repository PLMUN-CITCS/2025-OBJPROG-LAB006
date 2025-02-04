2025-OBJPROG-WK02S0E02
Week 02 - Introduction to Java Programming

Exercise # 05 - Guided Coding Exercise: Integrated Exercise – Circle Calculator

## **Instructions**

### **Step 1.1: Accept the Assignment**

   1. Click on the assignment link provided by your instructor.
   2. GitHub Classroom will create a **private repository** under your GitHub account.
   3. After the repository is created, click **"Go to Repository"** to view your assignment.

---

### **Step 1.2: Setup your Git Environment**
Only perform this if this is the first time you will setup your Git Environment

   1. Create a GitHub Account:
   ```bash
   https://github.com/signup?source=login
   ```
      
   2. Download and Install Git on your Laptop/Desktop:
   ```bash
   https://git-scm.com/downloads
   ```
   
   3. Create a Folder in your Laptop/Desktop
   4. Right-click anywhere in the created folder and select "Open Git Bash Here".
   5. In the Git Bash Terminal, set your git name, perform command:
   ```bash
   git config --global user.name "Your Name"
   ```
   
   6. In the Git Bash Terminal, set your git email, perform command:
   ```bash
   git config --global user.email "your.email@example.com"
   ```
   
   7. Create your SSH Key, just follow the instructions, no need to provide filename and passphrase. In the Git Bash Terminal, perform command:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
   
   8. Copy your SSH Keys into clipboard. In the Git Bash Terminal, perform command:
   ```bash
   clip < ~/.ssh/id_rsa.pub
   ```
   
   9. Log in to your GitHub account.
   10. In the upper-right corner of GitHub, click your profile picture and select Settings.
   11. In the left sidebar, click on SSH and GPG keys.
   12. Click the New SSH key button.
   13. In the Title field, give the key a recognizable name (e.g., "My Windows Laptop").
   14. In the Key field, CTRL + V or paste the keys copied into your clipboard. Save the key.
   15. Go Back to terminal, use command:
   ```bash
   ssh -T git@github.com
   ```

### **Step 2: Clone the Repository to Your Local Machine**

   1. On your repository page, click the green **"Code"** button.
   2. Copy the repository URL (choose HTTPS for simplicity).
   3. Open your terminal (or Git Bash, Command Prompt, or PowerShell) and run:
   
   ```bash
   git clone <git_repo_url>
   ```
   
   4. Navigate into the cloned folder:
   
   ```bash
   cd <git_cloned_folder>
   ```

### **Step 3: Complete the Assignment**

**Exercise # 05 - Utilizing the Java Math API Library**

   **Objective:**
   - Combine variable declarations, input/output, arithmetic expressions, operator precedence, type casting, and the Java `Math` API.
   - Calculate the area and circumference of a circle given a user-input radius.

   **File Naming Convention:**
   - `CircleCalculator.java`

   **Notable Observations (to be discussed after completing the exercise):**
   - This exercise combines several concepts you've learned, demonstrating how they can be used together in a practical program.
   - The `Math.PI` constant provides a precise value of π.
   - `Math.pow()` is used for exponentiation (raising a number to a power).
   - `System.out.printf()` is used for formatted output, which is essential for presenting results clearly.

   **Java Programming Best Practices:**
   - Use meaningful variable names.
   - Add comments to explain your code.
   - Close the `Scanner` object when you're finished with it.
   - Format your output to make it user-friendly.
   - Use appropriate data types (e.g., `double` for radius, area, and circumference).
      
   **Step-by-Step Instructions:**

   1. Import the Scanner Class
      - Create a file named `CircleCalculator.java`.
      - At the very top of your file (before the class declaration), import the `Scanner` class.  This allows you to get input from the user.
      ```Java
      import java.util.Scanner;
      ```
      
   2. Class and Main Method
      - Define the class `CircleCalculator` and its main method.
      ```Java
      public class CircleCalculator {
          public static void main(String[] args) {
      
          }
      }
      ```
            
   3. Create a Scanner Object
      - Inside the `main` method, create a `Scanner` object.  This object will be used to read user input from the console.
      ```Java
      Scanner input = new Scanner(System.in);
      ```

   4. Prompt for Radius
      - Use `System.out.print()` to prompt the user to enter the radius of the circle.
      ```Java
      System.out.print("Enter the radius of the circle: ");
      ```

   5. Read Radius Input
      - Use the `nextDouble()` method of your `Scanner` object to read the radius (which can be a decimal) and store it in a double variable named `radius`.
      ```Java
      double radius = input.nextDouble();
      ```

   6. Calculate Area
      - Declare a double variable named `area`.
      - Calculate the area of the circle using the formula: Area = π * r^2.  Use `Math.PI` for π and `Math.pow(radius, 2)` for r^2. Store the result in `area`.
      ```Java
      double area = Math.PI * Math.pow(radius, 2);
      ```

   7. Calculate Circumference
      - Declare a double variable named `circumference`.
      - Calculate the circumference of the circle using the formula: Circumference = 2 * π * r. Store the result in `circumference`.
      ```Java
      double circumference = 2 * Math.PI * radius;
      ```

   8. Output Results (Formatted)
      - Use `System.out.printf()` to print the `radius`, `area`, and `circumference`.  Format the output to two decimal places using `%.2f`.  Include descriptive labels.  `%n` creates a new line.
      ```Java
      System.out.printf("Radius: %.2f%n", radius);
      System.out.printf("Area: %.2f%n", area);
      System.out.printf("Circumference: %.2f%n", circumference);
      ```

   9. Demonstrate Operator Precedence
      - Close the `Scanner` object to release resources.
      ```Java
      input.close();
      ```

   10. Compile and Run
       - Save the file as `CircleCalculator.java`.
       - Compile the code using `javac CircleCalculator.java` in your terminal or command prompt.
       - Run the compiled code using `java CircleCalculator`.

### **Step 4: Push Changes to GitHub**
Once you've completed your changes, follow these steps to upload your work to your GitHub repository.

1. Check the status of your changes:
   Open the terminal and run:
   
   ```bash
   git status
   ```
   This command shows any modified or new files.
   
2. Stage the changes:
   Add all modified files to staging:
   
   ```bash
   git add .
   ```
   
3. Commit your changes:
   Write a meaningful commit message:
   
   ```bash
   git commit -m "Submitting OBJPROG Week 02 - Session 01 - Exercise 05"
   ```
   
4. Push your changes to GitHub:
   Upload your changes to your remote repository:
   
   ```bash
   git push origin main
   ```
