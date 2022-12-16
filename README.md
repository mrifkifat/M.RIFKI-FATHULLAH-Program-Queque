import java.util.*;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Queue<String> antrian = new LinkedList<>();
        Scanner input = new Scanner(System.in);

        System.out.println( "\n__________________");
        System.out.println( "| By M.RIFKI FATHULLAH |");
        System.out.println( "------------------\n");

        antrian.add("Muron");
        antrian.add("Dinda");
        antrian.add("Hoeron");
        antrian.add("Sarip");
        antrian.add("Cindy");

        System.out.print("\nDaftar Nama Antrian \t\t:" + antrian);
        System.out.print("\n\nMemanggil Antrian (y/n) \t: ");
        char hasil = input.next().charAt(0);

        if (hasil == 'y') {
            int size = antrian.size();
            for (int i=0; i < size; i++) {
                String panggil = antrian.poll();
                System.out.print("\nMemanggil Antrian \t\t\t:" + "[" + panggil + "]");
                System.out.print("\nDaftar Antrian Selanjutnya \t:" + antrian + "\n");
                if (antrian.size() == 0) {
                    System.out.print("\n\t||| Antrian Kosong |||\n\n");
                }
            }
        } else if (hasil == 'n') {
            System.out.println("\n\tBaik Terimakasi\n+++Sistem Dimatikan+++\n\n");
        } else {
            System.out.println("\n||| Input Anda Salah |||\n\n");
        }


    }
}
