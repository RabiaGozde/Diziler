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
