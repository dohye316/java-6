# java-6
方法重载
方法重载（overlord）
基本介绍
java中允许同一个类中， 多个同名方法的存在，但要求形参列表不一致！
比如：System.out.println(0; out 是PrintStream类型
重载的好处
1）减轻了起名的麻烦
2）减轻了记名的麻烦  下面calculate方法重载了
案例： MyCalculator 方法：calculator
calculate（int n1， int n2）两个整数的和
calculate（int n1， double n2）一个整数，一个double的和
calculate（double n2， int n1）一个double，一个int和
calculate（int n1，int n2， int n3）三个的和

class calculate{
	public static void main(String[] args) {
	MyCalculator mc =	new MyCalculator();
	System.out.println(mc.calculate(1.2));//执行第一个
    System.out.println(mc.calculate(1.1,2));//执行第三个	
	}
}
class MyCalculator{
	
    //下面的四个calculate 方法构成重载 
	public int calculate (int n1, int n2){//匹配的只有它
		return n1 + n2;
	}
	//两个整数的和
      public int calculate(int n1, double n2){
      return n1 + n2;
      }//一个整数，一个double的和
    public int calculaet(double n2, int n1){
       return n2 + n1;
       }//一个double，一个int和
    public int calculate(int n1,int n2,int n3){
        return n1 + n2 + n3；//三个的和
}
注意事项：
方法名必须要相同，不能calculate calculate1这么用
形参列表必须不同（形参类型或个数或顺序，至少有一样不同参数名无要求）形参名如n a要相同
可以一个是int 和另一个是void或是double
返回类型无要求
public int calculate (int n1, int n2){//
return n1 + n2;
	}
	//两个整数的和
      public int calculate(int a1, int a2){
      return a1 + a2;
//错误 没有构成重载，方法的重复定义



方法的重载
1.编写程序，类Methods中定义三个重载方法并调用。方法名为m。 三个方法分别接收一个int 参数，两个int参数， 一个字符串参数。分别执行平方运算并输出结果，相乘并输出结果，输出字符串信息。 在主类的main（）方法中分别参数区别调用三个方法
OverLoadExercise.java
class OverLoadExercise{

	public static void main(String[] args) {
		       Methods me = new Methods();
		    me.m(1);
		    me.m(1,2)  
		me.m("航顺平");
	}
}
class Methods{
	public int m(int n1){
		return n1*n1; 
		   
}
	
	public int m(int n1, int n2){
		return n1 + n2;
		
}
	
	public void m(String n1){
      System.out.print( n1);
	      
}
}


















2.在Methods类， 定义三个重载方法max（），第一个方法，返回两个int值中的最大值，第二个方法，返回两个double值中的最大值，第三个方法，返回三个double值中的最大值，并分别调用三个方法。

class OverLoadExercise{

	public static void main(String[] args) {
		       Methods me = new Methods();
		 System.out.println(me.max(2.5,5.1,133.4));
	}
}
class Methods{
	public int max(int n1,int n2){
		returnn n1 > n2 ? n1 : n2;
		   
}
	
	public double max(double n1, double n2){
		returnn n1 > n2 ? n1 : n2;
		
}
	
	public double max(double n1, double n2,double n3){
		if (n1 < n2&& n1 != n2) {
               if (n2 < n3&&n2 !=n3) {
               	      return n3;
               }else{
               	   return  n2;
               }
		}else{
             return n1;
		}
}
}














