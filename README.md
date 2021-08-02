package assignment_OOC;
import java.util.*;

class Branch {
	String branch;
	void read() {
		Scanner sc =new Scanner(System.in);
		System.out.println("Enter the Branch");
		branch=sc.next();	
	}
	void write() {
		System.out.println("Branch ::"+ this.branch);
	}
}
class Sem extends Branch {
	String sem;
	void read() {
		super.read();
		Scanner sc =new Scanner(System.in);
		System.out.println("Enter the Semister");
		sem=sc.next();	
	}
	void write() {
		super.write();
		System.out.println("Sem ::"+ this.sem);
	}
}
class Name extends Sem {
	String name;
	void read() {
		super.read();
		Scanner sc =new Scanner(System.in);
		System.out.println("Enter the Name");
		name=sc.next();	
	}
	void write() {
		super.write();
		System.out.println("Name ::"+ this.name);
	}
}
class USN extends Name {
	String usn;
	void read() {
		super.read();
		Scanner sc =new Scanner(System.in);
		System.out.println("Enter the USN");
		usn=sc.next();	
	}
	void write() {
		super.write();
		System.out.println("USN ::"+ this.usn);
	}
}

public class college {

	public static void main(String[] args) {
		Scanner sc= new Scanner(System.in);
		System.out.println("Enter the total no. of studen's database to be create");
		int n= sc.nextInt();
		USN s[]=new USN[n];
		for(int i=0;i<n;i++) {
			System.out.println("Student no."+(i+1));
			s[i]=new USN();
			s[i].read();
		}
		System.out.println();
		for(int i=0;i<n;i++) {
			s[i].write();
			System.out.println();
		}
		
	}

}
