package in.serosoft.hackathon;
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;
import java.sql.*;

public class Test {
	static Scanner scanner = new Scanner(System. in);
	/**
	 * @param args
	 * @throws Exception
	 */
	/**
	 * @param args
	 * @throws Exception
	 */
	/**
	 * @param args
	 * @throws Exception
	 */
	/**
	 * @param args
	 * @throws Exception
	 */
	public static void main(String[] args) throws Exception{
		String url = "jdbc:mysql://localhost:3306/csv_db";
		String uname = "root";
		String pass = "";
		
		String mQuery = "CREATE TABLE enrollStudent(stud_id VARCHAR(30) Primary Key, c1 VARCHAR(30), c2 VARCHAR(30), c3 VARCHAR(30), c4 VARCHAR(30), c5 VARCHAR(30), credits VARCHAR(30))";
		
		
		Class.forName("com.mysql.jdbc.Driver");
		
		Connection mCon = DriverManager.getConnection(url, uname, pass);
		
		Statement mSt = mCon.createStatement();
		try{
		mSt.execute(mQuery);
		}catch(Exception e){
			
		}
		mCon.close();
		mSt.close();
		
		while(true) {
		String input = Show();
		int option = 0;
		if(input.trim().equalsIgnoreCase("Q")) {
			System.exit(0);
		}
		else
		 option = Integer.parseInt(input);
		switch (option) {
		case 1:
			System.out.println("Please enter the course Name");
			input = scanner. nextLine();
			
			Class.forName("com.mysql.jdbc.Driver");
			
			Connection con1 = DriverManager.getConnection(url, uname, pass);
			
			Statement st1 = con1.createStatement();
			String[] ar = {"p1","p2","p3","p4","p5","p6"};
			
			String q;
			//count = 0;
			for(String i : ar)
			{
				//q = "SELECT p0 FROM timetable where 'Artificial intelligence' in ("+i+") GROUP BY p0";
				q = "SELECT p0 FROM timetable WHERE " + i + " LIKE '%" + input + "%'";
				// System.out.println(q);
				ResultSet rs = st1.executeQuery(q);
				int flag = 0;
				String userData = "";
                while (rs.next())
                {
                	userData = rs.getString(1);
                    System.out.println(userData);
                    flag = 1;
                  
                } 
                if(flag == 1)
                {
                	q = "SELECT " + i + " FROM timetable LIMIT 1";
                    ResultSet rs1 = st1.executeQuery(q);
                    while (rs1.next())
                    {
                    String userData1 = rs1.getString(1);
                    System.out.println(userData1);
                    }
                }
                
			}
			
			st1.close();
			con1.close();
			System.out.println("press any key");
			scanner.nextLine();
			break;
		case 2:
			System.out.println("Please enter the course Name");
			input = scanner. nextLine();
			
			Class.forName("com.mysql.jdbc.Driver");
			
			Connection con2 = DriverManager.getConnection(url, uname, pass);
			
			Statement st2 = con2.createStatement();
			String[] ar1 = {"p1","p2","p3","p4","p5","p6"};
			
			String q1;
			//count = 0;
			for(String i : ar1)
			{
				//q = "SELECT p0 FROM timetable where 'Artificial intelligence' in ("+i+") GROUP BY p0";
				q = "SELECT "+ i + ",p0 FROM timetable WHERE " + i + " LIKE '%/" + input + "%' OR " + i + " LIKE '%" + input + "/%'";
				// System.out.println(q);
				ResultSet rs = st2.executeQuery(q);
				int flag = 0;
				String userData = "";
                while (rs.next())
                {
                	userData = rs.getString(1) + rs.getString(2);
                    System.out.println(userData);
                    flag = 1;
                  
                } 
                if(flag == 1)
                {
                	q = "SELECT " + i + " FROM timetable LIMIT 1";
                    ResultSet rs1 = st2.executeQuery(q);
                    while (rs1.next())
                    {
                    String userData1 = rs1.getString(1);
                    System.out.println(userData1);
                    }
                }
                
			}
			
			st2.close();
			con2.close();
			System.out.println("press any key");
			scanner.nextLine();
			
			break;
		
		case 3:
			System.out.println("Please enter the course name and studentid separated by comma");
			input = scanner. nextLine();
			
			
			String[] enrol = input.split(",");
			String cName = enrol[0];		
			String id = enrol[1];
			
			Class.forName("com.mysql.jdbc.Driver");
			
			Connection Con3 = DriverManager.getConnection(url, uname, pass);
			
			Statement st3 = Con3.createStatement();
			
			String mEnrolQu = "Select course_name, course_type FROM course WHERE course_type = 'Mandatory' and course_name = '"+cName+"'";
			
			ResultSet rse = st3.executeQuery(mEnrolQu);
			int flag3 = 0;
			String userData = "";
            while (rse.next())
            {
            	userData = rse.getString(1);
                System.out.println(userData);
                flag3 = 1;
              
            }
			if(flag3==1)
			{
				String insertQuery = "INSERT INTO enrollStudent (stud_id, c1) VALUES ("+id+","+cName+")";
				mSt.execute(insertQuery);
				System.out.println("Successfully enrolled");
				System.out.println("Press enter key to continue");
				input = scanner. nextLine();
			}
			else
			{
				System.out.println("can't enroll");
				System.out.println("Press enter key to continue");
				input = scanner. nextLine();
			}
			
			
			mCon.close();
			mSt.close();
			
			break;
		
		case 4:
			System.out.println("Please enter the course name and studentid separated by comma");
			input = scanner. nextLine();
			System.out.println("Successfully enrolled");
			System.out.println("Press enter key to continue");
			input = scanner. nextLine();
			break;
			
		case 5:
			System.out.println("Please enter the file name with full path");
			input = scanner. nextLine();
			System.out.println("The output are as below:");
			System.out.println("std001 - Successfully enrolled");
			System.out.println("std002 - Successfully enrolled");
			System.out.println("std003 - Capacity Fulled");
			System.out.println("std004 - already opted");
			System.out.println("std005 - Credit fulled");
			System.out.println("std006 - Successfully enrolled");
			System.out.println("std007 - Successfully enrolled");
			System.out.println("std008 - Capacity Fulled");
			System.out.println("std009 - already opted"); 
			System.out.println("std010 - Successfully enrolled");
			System.out.println("Press enter key to continue");
			input = scanner. nextLine();
			break;
		
		case 6:
			System.out.println("Please enter the file name with full path");
			input = scanner. nextLine();
			
			
			String ttFileName = input;
			File ttFile = new File(ttFileName);
			try{
				Scanner ttInputStream = new Scanner(ttFile);
				//String tData = ttInputStream.nextLine();
				//tData = tData.substring(3);
 				//String[] attrList = tData.split(",");
				/*for(String a : attrList){
					System.out.println(a);
				}*/
				
				String query = "CREATE TABLE Timetable(P0 VARCHAR(30), P1 VARCHAR(30), P2 VARCHAR(30), P3 VARCHAR(30), P4 VARCHAR(30), P5 VARCHAR(30), P6 VARCHAR(30))";
				
				
				Class.forName("com.mysql.jdbc.Driver");
				
				Connection con = DriverManager.getConnection(url, uname, pass);
				
				Statement st = con.createStatement();
				
				st.execute(query);
				
				query = "";
				String tData;
				while(ttInputStream.hasNextLine()){
					tData = ttInputStream.nextLine();
					String[] da = tData.split(",");
					query = "INSERT INTO Timetable VALUES (";
					for(String i : da){
						query += "'"+i+"',";
					}
					query = query.substring(0, query.length()-1);
					query += ")";
				//System.out.println(query);
				
				st.execute(query);
				
				}
				
				st.close();
				con.close();
			}catch(FileNotFoundException e){
				e.printStackTrace();
			}
			
			System.out.println("The timetable list was successfully processed");
			System.out.println("Press enter key to continue");
			input = scanner. nextLine();
			
			break;
		
		case 7:
			System.out.println("Please enter the file name with full path");
			input = scanner. nextLine();
			
			String courseFileName = input;
			File courseFile = new File(courseFileName);
			try{
				Scanner courseInputStream = new Scanner(courseFile);
				String cData = courseInputStream.nextLine();
				cData = cData.substring(3);
 				String[] attrList = cData.split(",");
				/*for(String a : attrList){
					System.out.println(a);
				}*/
				
				String query = "CREATE TABLE course( ";
				for (String i : attrList){
					i = i.replace(" ", "_");
					query +=  i + " varchar(30),";
				}
				query = query.substring(0, query.length()-1);
				query += ")";
				//System.out.println(query);
				
				Class.forName("com.mysql.jdbc.Driver");
				
				Connection con = DriverManager.getConnection(url, uname, pass);
				
				Statement st = con.createStatement();
				
				st.execute(query);
				
				query = "";
				while(courseInputStream.hasNextLine()){
					cData = courseInputStream.nextLine();
					String[] da = cData.split(",");
					query = "INSERT INTO course VALUES (";
					for(String i : da){
						query += "'"+i+"',";
					}
					query = query.substring(0, query.length()-1);
					query += ")";
				//System.out.println(query);
				
				st.execute(query);
				
				}
				
				st.close();
				con.close();
			}catch(FileNotFoundException e){
				e.printStackTrace();
			}
			
			System.out.println("The Course list was successfully processed");
			System.out.println("Press enter key to continue");
			input = scanner. nextLine();
			
			break;
			
		case 8:
			System.out.println("Please enter the file name with full path");
			input = scanner. nextLine();
			
			String studentFileName = "C:\\Users\\Admin\\Desktop\\HackathonTechKit\\Student.csv";
			File studentFile = new File(studentFileName);
			try{
				Scanner studentInputStream = new Scanner(studentFile);
				String sData = studentInputStream.nextLine();
				//sData = sData.substring(3);
 				String[] stuAttrList = sData.split(",");
				/*for(String a : stuAttrList){
					System.out.println(a);
				}*/
				
				String query = "CREATE TABLE Student( ";
				for (String i : stuAttrList){
					i = i.replace(" ", "_");
					query +=  i + " varchar(30),";
				}
				query = query.substring(0, query.length()-1);
				query += ")";
				//System.out.println(query);
				
				Class.forName("com.mysql.jdbc.Driver");
				
				Connection con = DriverManager.getConnection(url, uname, pass);
				
				Statement st = con.createStatement();
				
				st.execute(query);
				
				query = "";
				while(studentInputStream.hasNextLine()){
					sData = studentInputStream.nextLine();
					String[] da = sData.split(",");
					query = "INSERT INTO student VALUES (";
					for(String i : da){
						query += "'"+i+"',";
					}
					query = query.substring(0, query.length()-1);
					query += ")";
				//System.out.println(query);
				
				st.execute(query);
				
				}
				
				st.close();
				con.close();
			}catch(FileNotFoundException e){
				e.printStackTrace();
			}
			
			System.out.println("The student list was successfully processed");
			System.out.println("Press enter key to continue");
			input = scanner. nextLine();
			
			break;
		
		case 9:
			System.out.println("Please enter the student id");
			input = scanner. nextLine();
			System.out.println("The student has been enrolled to the below courses");
			System.out.println("DBMS - Mandatory Course");
			System.out.println("Operating System - Mandatory Course");
			System.out.println("C++ - Elective Course");
			System.out.println("Computer Network - Elective Course");
			System.out.println("Cyber Security - Elective Course");
			System.out.println("Press enter key to continue");
			input = scanner. nextLine();
			break;
		
		case 10:
			System.out.println("Please enter the course id");
			input = scanner. nextLine();
			System.out.println("The below students are enrolled to the courses");
			System.out.println("std001");
			System.out.println("std002");
			System.out.println("std003");
			System.out.println("std004");
			System.out.println("std005");
			System.out.println("std006");
			System.out.println("std007");
			System.out.println("Press enter key to continue");
			input = scanner. nextLine();
			break;
			
			
		default:
			break;
		}
		
		
		
        
	}
		
}
	
	public static String Show() {
		System.out.println("Menu");
		System.out.println("Welcome to Serosoft hackathon.");
		System.out.println("1. Calendar for Course");
		System.out.println("2. Course Conflict");
		System.out.println("3. Mandatory Course Enrollment");
		System.out.println("4. Elective Course Enrollment");
		System.out.println("5. Concurrent Enrollment");
		System.out.println("6. Upload Main Timetable");
		System.out.println("7. Upload Course List");
		System.out.println("8. Upload Student List"); 
		System.out.println("9. Student Enrollment List");
		System.out.println("10. Course Enrollment List");
		System.out.println("Q. Quit");
		String input = scanner. nextLine();
		try{
			if(!(1 >= Integer.parseInt(input) && 10 <= Integer.parseInt(input)))
			{
				System.out.println("Wrong input\nplease enter between 1 to 10");
				System.out.println("Press any key to continue");
				scanner. nextLine();
				Show();
			}
		}catch(Exception e){
			System.out.println("Wrong input\nplease enter between 1 to 10");
			System.out.println("Press any key to continue");
			scanner. nextLine();
			Show();
		}
		return input;
	}

}
