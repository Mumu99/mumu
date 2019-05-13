# mumu
关于木木大神的个人存储库
数据库
	public static void main（String [] args）{
        // TODO Auto-generated method stub
	 //1.加载驱动
	 String driverName="com.microsoft.sqlserver.jdbc.SQLServerDriver";
     String url="jdbc:sqlserver://localhost:1433;databaseName=NetStore_sql";
     String user="sa";//超级管理员
     String password="123456";//密码
     try
     {
     Class.forName(driverName);
     System.out.println("加载驱动成功！");
     }catch(Exception e){
     e.printStackTrace();
     System.out.println("加载驱动失败！");
     }
     try{
    	 Connection dbConn=DriverManager.getConnection(url,user,password);
    	 System.out.println("连接数据库成功！");
    	 }catch(Exception e)
    	 {
    	 e.printStackTrace();
    	 System.out.print("SQL Server连接失败！");
    	 }
    }
