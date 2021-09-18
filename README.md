# Matriz- Area-Inferior-Java
Ler um caractere maiúsculo, que indica uma operação que deve ser realizada e uma matriz M[12][12]. Em seguida, calcule e mostre a soma ou a média considerando somente aqueles elementos que estão na área inferior da matriz, conforme ilustrado abaixo (área verde)

import java.util.Scanner;

public class Matrizinferior {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double m[][] = new double[12][12];
        double sum = 0;
        int count = 0;
        String v = sc.next();
        for (int i = 0; i < m.length; i++) {
            for (int j = 0; j < m.length; j++) {
                double x = sc.nextDouble();
                m[i][j] = x;
                if (j < i && j > (m.length - i - 1)) {
                    sum += x;
                    count++;
                }
            }
        }
        if (v.equals("S")) {
            System.out.printf("%.1f\n", sum);
        } else {
            System.out.printf("%.1f\n", (sum / count));
        }
    }
