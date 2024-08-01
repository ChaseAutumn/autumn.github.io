#这是一篇笔记
  import java.util.*;
public class Main{
    public static void main(String args[]){    //主函数
        Scanner scanner=new Scanner(System.in);//1.输入数据
        int n=scanner.nextInt();                 
        System.out.println(fib(n));            //2.打印结果
    }
    public static int fib(int n){//函数1
        int []count=new int[n+1];//1.声明数组
        if(n<1) return 0;        //（（（2.如果输入不符合）））
        return helper(count,n);  //2.使用函数
        }

    public static int helper(int []count,int n) {//函数2
            if (count[n] != 0)                   //（（（1.如果结果非0，则输出）））
                return count[n];                 
            if (n == 1 || n == 2)                //2.设置边界线
                return 1;
            count[n] = helper(count,n-1) + helper(count,n - 2);//3.递归 4.求最值
        return count[n];
    }
}
//1 1 2 3 5 8
