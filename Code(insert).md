Import java.sql.*;
Public class DataB{
Static final String JDBC_Driver = “.com.sql.jdbc.Driver”;
Static final String DB_Url=“C:/drawings/school1.accdb”;
static final String USER = "username”;
Static final String PASS = “password”;

public static void main(String[] args) {
Connection conn = null;
Statement stmt = null;
try{
  Class.forName("com.mysql.jdbc.Driver");
  System.out.println("Connecting to a selected database...");
  conn = DriverManager.getConnection(“C:/drawings/school1.accdb”, “username”, “password”);
  System.out.println("Database connection is successfully");
System.out.println("Inserting records into the table...");
      stmt = conn.createStatement();
String sql = “INSERT INTO tblLearnersDetails” + 
“Values (‘Esona’, ‘Dyakalashe’, ‘0627690213’, 
‘Makhaza’ , ‘Female’, ‘11’ , ‘ed01’);
Stm executeUpdate(sql);
System.out.printLn(“the recored is inserted”);
 }catch(SQLException se){
 Se.printStackTrace();
}
}




 
