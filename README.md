# Diziler
## Harmonik Ort
public class Main {
    public static void main(String[] args) {
      
      int[] numbers = {1, 2, 3, 4, 5};
      double sum = 0.0;
      for (int i = 0; i < numbers.length; i++) {
        sum += (1.0 / numbers[i]);
        
      }
      System.out.println(numbers.length/sum);
    }
}
## Max Min
public class Main {
    public static void main(String[] args) {
        int[] list = {56, 34, 1, 8, 101, -2, -33};
      
        int min = list[0];
        int max = list[0];

        for (int i : list) {
            if (i < min) {
                min = i;
            }
            if (i > max) {
                max = i;
            }
        }

        System.out.println("Minimum Değer " + min);
        System.out.println("Maximum Değer " + max);

    }
}
## Çok boyutlu diziler kullanılarak "yıldızlar" ile ekrana "B" harfi yazan program
public class Main {
    public static void main(String[] args) {
        String[][] letter = new String[7][4];

        for (int i = 0; i < letter.length; i++) {
            for (int j = 0; j < letter[i].length; j++) {
                if (i == 0 || i == 3 || i==letter.length-1) {
                    letter[i][j] = " * ";
                } else if (j == 0 || j == 3) {
                    letter[i][j] = " * ";
                } else {
                    letter[i][j] = "   ";
                }
            }
        }

        for (String[] row : letter){
            for (String col : row){
                System.out.print(col);
            }
            System.out.println();
        }
    }
}
## Dizideki Elemanları Sıralama
import java.util.Scanner;
import java.util.Arrays;
 
public class Main {
    
    public static void main(String[] args) {
        
        Scanner scan = new Scanner(System.in);

      System.out.print("Bir Sayıyı giriniz: ");
      int a = scan.nextInt();
        
      int [] dizi = new int[a];
        
        
      for(int i = 0; i < dizi.length; i++)
      {
          System.out.print((i+1) + ". Sayıyı giriniz: ");
          dizi[i] = scan.nextInt();
            
      }
      Arrays.sort(dizi);  
      System.out.println(Arrays.toString(dizi));
    }
}
## Dizideki Tekrar Eden Sayıları Bulan Program
import java.util.Scanner;
import java.util.Arrays;
 
public class Main {
  static boolean isFind(int[] arr,int value){
    for (int i:arr){
      if(i==value){
        return true;
      }
    }
    return false;
  }
    
  public static void main(String[] args) {
        
    int sayac=0;
    int sayac2=0;
    
    int[]dizi={10, 20, 20, 10, 10, 20, 5, 20};
    int[]frekans=new int[dizi.length];
                
    for(int i=0;i<dizi.length;i++){
      for(int j=0;j<dizi.length;j++){
        if((i!=j)&&(dizi[i]==dizi[j])){
          if(!isFind(frekans, dizi[i])){
            frekans[sayac++]=dizi[i];
            
          }
          
          break;
        }
        
      }
               
    }
    for(int value: frekans){
      if(value!=0){
        System.out.println(value);
      }
    }    
  }
}
## Matris Transpozunu Bulma
import java.util.Scanner;
 
public class Main {
  public static void main(String[] args) {

    int m, n, c, d;
    Scanner in = new Scanner(System.in);
    System.out.println("Matrisin satır ve sütun sayılarını girin");
    m = in.nextInt();
    n = in.nextInt();

    int matrix[][] = new int[m][n];
    System.out.println("Matrisin elemanlarını girin");
    
    for (c = 0; c < m; c++)
      for (d = 0; d < n; d++)
        matrix[c][d] = in.nextInt();

    for (int row = 0; row < matrix.length; row++) {
    for (int column = 0; column < matrix[row].length; column++) {
       System.out.print(matrix[row][column] + " "); 
  }
    System.out.println(); 
  }
    int transpose[][] = new int[n][m];
    for (c = 0; c < m; c++)
      for (d = 0; d < n; d++)
        transpose[d][c] = matrix[c][d];

    System.out.println("Matrisin tersi:");

    for (c = 0; c < n; c++)
    {
      for (d = 0; d < m; d++)
        System.out.print(transpose[c][d]+"\t");

      System.out.print("\n");
    }
  }
}
