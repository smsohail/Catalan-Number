# Catalan-Number
import java.util.*;
public class CatalanN {
	public static void main(String[] args){
		Scanner input = new Scanner(System.in);
		int T[] = new int[100];
		T[0]=1;
		T[1]=1;
		int  n = input.nextInt();
		for(int i=2;i<=n;i++){
			for(int j=0;j<i;j++){
				T[i]+=T[j]*T[i-j-1];
				
			}
		}
		for(int i=0;i<=n;i++){
			System.out.println(T[i]);
		}
		
		input.close();
	}
}
