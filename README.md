import java.util.Scanner;
public class Contabanco {
    public static void main(String[] args) {
        long numero = 1021;
        String agencia = "067-8";
        Scanner scanner = new Scanner(System.in);
        double saldo = 234.78;
        System.out.println("Digite o seu nome: "); 
        String nome = scanner.nextLine();
        System.out.println("Ola " + nome + ", Obrigado por criar uma conta em nosso banco, sua agencia é "+ agencia +", conta "+ numero +" e seu saldo é "+ saldo);
        scanner.close();
    }         
