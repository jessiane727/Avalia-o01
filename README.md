import java.util.Scanner;

public class SistemaEscolar {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        double[] notas = new double[8]; // 8 notas (2 por bimestre)
        double[] mediasBimestrais = new double[4]; // 4 médias bimestrais

        // Entrada das notas
        System.out.println("Digite as 8 notas do aluno (duas por bimestre):");
        for (int i = 0; i < 8; i++) {
            System.out.print("Nota " + (i + 1) + ": ");
            notas[i] = input.nextDouble();
        }

        // Cálculo das médias dos bimestres
        for (int i = 0; i < 4; i++) {
            mediasBimestrais[i] = (notas[i * 2] + notas[i * 2 + 1]) / 2;
        }

        // Cálculo das médias semestrais
        double mediaSemestre1 = (mediasBimestrais[0] + mediasBimestrais[1]) / 2;
        double mediaSemestre2 = (mediasBimestrais[2] + mediasBimestrais[3]) / 2;

        // Cálculo da média final
        double mediaFinal = (mediaSemestre1 + mediaSemestre2) / 2;

        // Exibição dos resultados formatados
        System.out.println("\n--- Resultados ---");
        System.out.printf("1°Bimestre: %.1f, ", mediasBimestrais[0]);
        System.out.printf("2°Bimestre: %.1f, ", mediasBimestrais[1]);
        System.out.printf("3°Bimestre: %.1f, ", mediasBimestrais[2]);
        System.out.printf("4°Bimestre: %.1f, ", mediasBimestrais[3]);
        System.out.printf("1° Semestre: %.1f, ", mediaSemestre1);
        System.out.printf("2° Semestre: %.1f, ", mediaSemestre2);
        System.out.printf("Media final: %.1f\n", mediaFinal);

        input.close();
    }
}
****
