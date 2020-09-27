# Min-in-array
Array challenge

import java.util.Scanner;

public class Main {

    private static Scanner scanner = new Scanner(System.in);
    public static void main(String[] args) {
        int[] myIntArray = readIntegers(10);
        System.out.println(findMin(myIntArray));

    }


    public static int[] readIntegers(int count){
        int[] array = new int[count];
        System.out.println("Enter " + count + " integer values: \r");
        for(int i = 0; i< array.length;i++){
            array[i] = scanner.nextInt();
        }
        return array;
    }

    public static int findMin(int[] array){
        int min = 0;

        for(int i = 0; i< array.length - 1;i++){
            if(array[i] > array[i+1]){
                min = array[i + 1];
            }
        }
        return min;
    }
}
