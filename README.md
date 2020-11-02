# shiyan2

JAVA实验：面向对象编写学生选课模拟系统

实验目的：
初步了解分析需求，从学生选课角度了解系统中的实体及其关系，学会定义类中的属性以及方法；
掌握面向对象的类设计方法（属性，方法）；
掌握类的继承用法，通过构造方法实例化对象；
学会使用super（），用于实类化子类；
掌握使用Object根类的toString（）方法，应用在相关对象的信息输出中。

实验要求：
1、编写要求的实体类以及测试类（注意类之间继承关系的适用）
2、在测试主类中，实列化多个类实体，模拟学生选课操作，打印课程信息（信息包括：编号、课程名称、上课地点、时间、授课老师等）；模拟学生退课操作，再打印课程信息；
3、编写实验报告（要求有实验目的、要求、过程图、核心代码、注释、系统运行截图、编程感悟等，分章节罗列，不能在实验中粘贴大段代码）；

实验过程：
1、功能划分：
1）人员信息 （编号、姓名、性别等）
2）教师及课程信息（编号、姓名、性别、所授课程）
3）学生信息（编号、姓名、性别、所选课程）
4）课程信息（编号、课程名称、上课地点）


一、对人员信息进行编写录入：
public class People {
	private int id；//对编号进行定义
	private String peopleName;//定义人员姓名
	private String peopleSex;//性别定义
	public People(int id,String peopleName,String peopleSex)
  {
		this.id=id;
		this.peopleName=peopleName;
		this.peopleSex=peopleSex；
            …………}
 二、教师以及课程信息编写：
 public class Teacher 
 {
	private int teaId;//教师编号编写
	private String teaName;//教师名称
	private String teaSex;//教师性别
	private Course[]courses;//所授课程
	public Teacher() {
		super();
		courses=new Course[3];
            …………}

三、学生信息编写
public class Student 
{
	private int stuId;//学生学号编写
	private String stuName;//学生姓名编写
	private String stuSex;//学生性别
	private Course[] courses;//学生所选课程
	public Student() {
		super();
		courses=new Course[3];
	}
	public Student(int stuId,String stuName,String stuSex) {
		super();
		this.stuId=stuId;
		this.stuName=stuName;
		this.stuSex=stuSex;
		courses=new Course[3];
           …………
	}


四、课程信息编写
public class Course
{
	 private String courseName;//课程名称
	 private int courseId;//课程编号
	 private Teacher teacher;//教授该课程的教师
	 private float credit;
	 private Student[] students;
	 public Course(int courseId,String courseName,float credit,Teacher teacher) 
          ………
                }
	
 
            
