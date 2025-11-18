# Opera-es-Portas-Logicas-em-sa-da-Java
Operações Portas Logicas em saída Java
import java.util.Scanner;

public class OperacoesLogicas {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int opcao;

        do {
            System.out.println(" ~~~~~~ MENU ~~~~~~ ");
            System.out.println("1 - AND");
            System.out.println("2 - OR");
            System.out.println("3 - NOT");
            System.out.println("0 - Sair");
            System.out.print("Escolha uma opção: ");

            opcao = sc.nextInt(); 

            switch (opcao) {

                case 1: 
                    System.out.print("Digite o primeiro valor (0 ou 1): ");
                    int a1 = sc.nextInt();
                    System.out.print("Digite o segundo valor (0 ou 1): ");
                    int b1 = sc.nextInt();
                    int resultadoAnd = (a1 == 1 && b1 == 1) ? 1 : 0;
                    System.out.println("Resultado: " + a1 + " AND " + b1 + " = " + resultadoAnd);
                    System.out.println();
                    break;

                case 2: 
                    System.out.print("Digite o primeiro valor (0 ou 1): ");
                    int a2 = sc.nextInt();
                    System.out.print("Digite o segundo valor (0 ou 1): ");
                    int b2 = sc.nextInt();
                    int resultadoOr = (a2 == 1 || b2 == 1) ? 1 : 0;
                    System.out.println("Resultado: " + a2 + " OR " + b2 + " = " + resultadoOr);
                    System.out.println();
                    break;

                case 3: 
                    System.out.print("Digite um valor (0 ou 1): ");
                    int a3 = sc.nextInt();
                    int resultadoNot = (a3 == 1) ? 0 : 1;
                    System.out.println("Resultado: NOT " + a3 + " = " + resultadoNot);
                    System.out.println();
                    break;

                case 0:
                    System.out.println("Saindo...");
                    break;

                default:
                    System.out.println("Opção inválida!\n");
            }

        } while (opcao != 0); 

        sc.close();
    }
}
