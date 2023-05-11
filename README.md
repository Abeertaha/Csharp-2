

using System;

class Employee {
    public string? Name;
    public int Age;
    public double Salary;
    public double CalculateSalary() {
        double salary = 600;
        if (Age >= 50) {
            salary += 1000;
        }
        return salary;
    }
}

class Program {
    static void Main() {
        Employee[] employees = new Employee[3];
        
        employees[0] = new Employee { Name = "Julia", Age = 46, Salary = 500};
        employees[1] = new Employee { Name = "Ali", Age = 50, Salary = 600};
        employees[2] = new Employee { Name = "Adam", Age = 60, Salary = 700};

        foreach (Employee employee in employees) {
            double salary = employee.CalculateSalary();
            Console.Write(employee.Name + " earning " + salary);
            if (employee.Age >= 50) {
                Console.Write(" age " + employee.Age);
            }
            Console.WriteLine();
        }
    }
}
