Verilen sql tablosunda belirttiğim bölümlerde düzenleme yaptım.:

-- Departments tablosunun oluşturulması ve veri eklenmesi
CREATE TABLE Departments (
    DepartmentID INT PRIMARY KEY,
    **DepartmentName VARCHAR(50) NOT NULL UNIQUE**
);

INSERT INTO Departments (DepartmentID, DepartmentName) VALUES
(1, 'IT'),
(2, 'HR'),
(3, 'Finance');

-- Employees tablosunun oluşturulması ve veri eklenmesi
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Age INT,
   **DepartmentName VARCHAR(50) NOT NULL,** 
    Salary DECIMAL(10,2),
    JoinDate DATE,
    **FOREIGN KEY (DepartmentName) REFERENCES Departments(DepartmentName) ** 
