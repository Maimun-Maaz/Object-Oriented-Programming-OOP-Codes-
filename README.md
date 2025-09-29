# Object-Oriented-Programming-OOP-Codes-
#Task-01
we are given the following “University” class: 

public class University{
    public String name;
    public String country;
}
Now writing a Java tester class named “UniversityTester”.

a.Write the main method and create 2 objects of University class and print the location of the objects and print the instance variables of the objects. Are the location of the objects the same? 

b.Now change the instance variables of the first object.
 name =  “Imperial College London”
 country = “England”

Now change the instance variables of the second object.
	name =  “BRAC University”
country = “Bangladesh”

public class UniversityTester{
  public static void main(String[] args){
    University u1=new University();
    University u2=new University();
    
    System.out.println(u1);
    System.out.println(u2);
    System.out.println(u1.name);
    System.out.println(u1.country);
    System.out.println(u2.name);
    System.out.println(u2.country);
    u1.name="Imperial College of London";
    u1.country="England";
    u2.name="Brac university";
    u2.country="Bangladesh";
    System.out.println(u1.name);
    System.out.println(u1.country);
    System.out.println(u2.name);
    System.out.println(u2.country);
  }
}
public class University{
    public String name;
    public String country;
}
#Task-02
Design the “Student” class so that the main method prints the following:
public class StudentTester2{
   public static void main(String [] args){
      Student s1 = new Student();
      System.out.println("Name of the Student: "+s1.name);
      System.out.println("ID of the Student: "+s1.id);
      s1.name = "Bob";
      s1.id = 123;
      System.out.println("Name of the Student: "+s1.name);
      System.out.println("ID of the Student: "+s1.id);
   }
}

public class Student{
  public String name;
  public int id;
}

#Task-03
Design the Course class to generate the correct output from the driver code provided 
public class Tester3{
  public static void main(String[] args) {
    Course c1 = new Course();
    Course c2 = new Course();  
    c1.updateDetails("Programming Language I","CSE110", 3);
    System.out.println("========== 1 ==========");
    c1.displayCourse(); 
    c2.updateDetails("Data Structures","CSE220", 3);
    System.out.println("========== 2 ==========");
    c2.displayCourse();  
    c1.updateDetails("Programming Language II","CSE111", 3);
    System.out.println("========== 3 ==========");
    c1.displayCourse();
  }
}
public class Course{
  public String name;
  public String code;
  public int credit;
  
  public void updateDetails(String a,String b,int c){
    name=a;
    code=b;
    credit=c;
  }
  
  public void displayCourse(){
    System.out.println("Course Name: "+name);
    System.out.println("Course Code: "+code);
    System.out.println("Course Credit: "+credit);
  }
}

#Tasks-04
Design the CellPhone class so that the main method of tester class can produce the following output:
public class Tester4{
  public static void main(String[]args){
     CellPhone phone1 = new CellPhone();
     phone1.printDetails();
     phone1.model ="Nokia 1100";
     System.out.println("1##################");
     phone1.storeContact("Joy - 01834");
     System.out.println("===================");
     phone1.printDetails();
     System.out.println("2##################");
     phone1.storeContact("Toya - 01334");
     phone1.storeContact("Aayan - 01135");
     System.out.println("===================");
     phone1.printDetails();
     System.out.println("3##################");
     phone1.storeContact("Sani - 01441");
     System.out.println("===================");
     phone1.printDetails();  
  }
}

public class CellPhone{
  public String model="unknown";
  public String [] arr1= new String [3];
  public int number;
  
  public void printDetails(){
    if(number==0){
    System.out.println("Phone Model "+model);
    System.out.println("Contacts Stored "+number);
    }
    else{
    System.out.println("Phone Model "+model);
    System.out.println("Contacts Stored "+number);
    System.out.println("Stored Contacts :");
    for(int i=0;i<number;i++){
      System.out.println(arr1[i]);
    }
  }
  }
  
  public void storeContact(String a){
    if(number<3){
    arr1[number]=a;
    number++;
    System.out.println("Contact Stored");
  }
    else {
      System.out.println("Memory full. New contact can't be stored.");
    }
  }
}

#Task-05
Consider the following class:
public class Human{
    public int age;
    public double height;
}
public class main{
public static void main(string {} args){
	Human h1 = new Human();
	Human h2 = new Human();
	h1.age = 21;
	h1.height = 5.5;
	System.out.println(h1.age);
	System.out.println(h1.height);
	h2.height = h1.height - 3;
	System.out.println(h2.height);
	h2.age = h1.age++;
	System.out.println(h1.age);
	h2 = h1;
	System.out.println(h2.age);
	System.out.println(h2.height);
	h2.age++;
	h2.height++;
	System.out.println(h1.age);
	System.out.println(h1.height);
	h1.age = ++h2.age;
	System.out.println(h2.age);
	System.out.println(h2.height);	
}
#Task-06
Design the CSECourse class to generate the correct output from the driver code provided below:
public class CourseTester{
  public static void main(String args []){
    CSECourse c1 = new CSECourse();
    System.out.println("Course Name: "+c1.courseName);
    System.out.println("Course Code: "+c1.courseCode);
    System.out.println("Credit: "+c1.credit);
   }
}
public class CSECourse{
  public String courseName="Programming Language II";
  public String courseCode="CSE111";
  public int credit=3;
}

#Task-07
Design the “ImaginaryNumber”  class to generate the output given below:
public class Tester7{
  public static void main(String [] args){
     ImaginaryNumber num1 = new ImaginaryNumber();
     String p = num1.printNumber();
     System.out.println(p);
     System.out.println("1********");
     num1.realPart=3;
     num1.imaginaryPart=7;
     System.out.println(num1.printNumber());
     System.out.println("2********");
     ImaginaryNumber num2 = new ImaginaryNumber();
     num2.realPart=1;
     num2.imaginaryPart=9;
     System.out.println(num2.printNumber());
    }
}
public class ImaginaryNumber{
  public int realPart=0;
  public int imaginaryPart=0;
  
  public void printNumber(){
    System.out.println(realPart+" + "+imaginaryPart+"i");
  }
}


    
    
  

                         
    




Now check if the instance variables of both objects have changed or not and whether the instance variables of both objects are of the same value or not.
