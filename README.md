import java.util.Scanner;

public class cardEx {
	public static void main(String[] args) {
		//Java
		Scanner scanner=new Scanner(System.in);
		
		System.out.println("M,N 입력 ");
		int M=scanner.nextInt();
		int N=scanner.nextInt();
		
		int [][]array= new int[N][M];
		
		for(int i=0;i<N;i++)
			for(int j=0;j<M;j++)
			{
				array[i][j]=scanner.nextInt();
			}
		int[] min=new int[N];
		for(int j=0;j<N;j++)
		for(int i=0;i<M;i++)
		{
			min[j]=array[j][0];
			if(min[j]>=array[j][i])
				min[j]=array[j][i];
		}
		int max=0;
		for(int i=0;i<N;i++)
		{
			max=min[0];
			if(max<=min[i])
				max=min[i];
		}
		System.out.println(max);
			
		
		
	}

}
