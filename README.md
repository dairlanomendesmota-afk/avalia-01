import java.util.Scanner;

public class SistemaEscolar {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        double[] notas = new double[8];
        
        // Lê as 8 notas anuais
        System.out.println("Digite as 8 notas anuais do aluno:");
        for (int i = 0; i < 8; i++) {
            System.out.print("Nota " + (i + 1) + ": ");
            notas[i] = scanner.nextDouble();
        }
        
        // Calcula as médias bimestrais
        double media1Bim = (notas[0] + notas[1]) / 2;
        double media2Bim = (notas[2] + notas[3]) / 2;
        double media3Bim = (notas[4] + notas[5]) / 2;
        double media4Bim = (notas[6] + notas[7]) / 2;
        
        // Calcula as médias semestrais
        double media1Sem = (media1Bim + media2Bim) / 2;
        double media2Sem = (media3Bim + media4Bim) / 2;
        
        // Calcula a média final
        double mediaFinal = (media1Sem + media2Sem) / 2;
        
        // Exibe os resultados
        System.out.println("\n========== RESULTADOS ==========");
        System.out.printf("1° Bimestre: %.1f%n", media1Bim);
        System.out.printf("2° Bimestre: %.1f%n", media2Bim);
        System.out.printf("1° Semestre: %.1f%n", media1Sem);
        System.out.println("---------------------");
        System.out.printf("3° Bimestre: %.1f%n", media3Bim);
        System.out.printf("4° Bimestre: %.1f%n", media4Bim);
        System.out.printf("2° Semestre: %.1f%n", media2Sem);
        System.out.println("---------------------");
        System.out.printf("Média Final: %.1f%n", mediaFinal);
        
        scanner.close();
    }
}
