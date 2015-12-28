# acadgild-assignment-session-3
Assignment 1
import java.util.Scanner;

public class CubeRtSqrRt {

	public static void main(String[] args) {
		int num;
		double cuberoot,squareroot;
		System.out.println("This program is to calculate Cube root & Square root of a given Number");
		System.out.print("Enter a number: ");
		Scanner in=new Scanner(System.in);
		num=in.nextInt();
		cuberoot=Math.cbrt(num);
		squareroot=Math.sqrt(num);
		System.out.println("The Cube Root is: "+cuberoot);
		System.out.println("The Square Root is: "+squareroot);
	}

}

Assignment 2

public class CheckPrimeNum {
	int num;
	@Override
	public String toString() {
		return "CheckPrimeNum [num=" + num + "]";
	}
	CheckPrimeNum(int num)
	{
		this.num=num;
		int a=2;
		 if(num==2)
		{
			System.out.println(num+" is a prime number");
		}
		else
		{
			while(num%a!=0 && num-1>a)
			{
				a++;
			}
			if(num==1 || num==0)
			{
				System.out.println(num+" Not a prime number");
			}
			else if (num % a == 0)
			{
				System.out.println(num+" Not a prime no.Since Divisible it is by: "+a+" hence, it is a composite no.");
			}		
			else
			{
				System.out.println(num+" is a prime number");
				
			}
		}

    }
	
}

public class DemoCheckPrimeNum {

	public static void main(String[] args) {
		CheckPrimeNum c1=new CheckPrimeNum(33);
		System.out.println(c1);

	}

}
Assignment 3

public class Employee {
	String name;
	int age;
	float salary;
	static String companyname="ACADGILD";
	Employee(){
		name="xyz";
		age=29;
		salary=(float) 10000.00;
	}
	Employee(String name,int age,float salary){
		this.name=name;
		if(age>=1&&age<=100){
		this.age=age;
		return;
		}
		else{
		System.out.println("invalid age");
		this.age=0;
		}
		this.salary=salary;
	}
	@Override
	public String toString() {
		return "Employee [name=" + name + ", age=" + age + ", salary=" + salary + ", Companyname=" +companyname+"]";
	}
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public int getAge() {
		return age;
	}
	public void setAge(int age) {
		if(age>=1&&age<=100){
			this.age=age;
			return;
			}
			else{
			System.out.println("invalid age");
			this.age=0;
			}
	}
	public float getSalary() {
		return salary;
	}
	public void setSalary(float salary) {
		this.salary = salary;
	}
	public static String getCompanyname() {
		return companyname;
	}
	public static void setCompanyname(String companyname) {
		Employee.companyname = companyname;
	}
	
	
}

public class DemoEmployee {

	public static void main(String[] args) {
		Employee e1=new Employee("arvind",240,(float)10000.57);
		Employee e2=new Employee();
		System.out.println(e1+"\n"+e2);
		e2.setName("qrs");
		e1.setAge(24);
		System.out.println(e2.getName());
		System.out.println(e1.getAge());
		System.out.println(e1+"\n"+e2);
		Employee.setCompanyname("Java Acadgild");
		System.out.println(e1+"\n"+e2);
		
	}

}
