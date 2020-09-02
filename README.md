import java.util.Scanner;

public class SmartLily {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        int LilyAge = Integer.parseInt(scanner.nextLine());
        double WashingMachinePrice = Double.parseDouble(scanner.nextLine());
        int SingleToyPrice = Integer.parseInt(scanner.nextLine());
        int ToyCount = 0;
        double TotalBdayMoney = 0;

        for (int i = 1; i <= LilyAge; i++){
            if (!(i % 2 == 0)){
                ToyCount ++;
            }
            else {
                TotalBdayMoney = TotalBdayMoney + ((i/2 )*10);
                TotalBdayMoney = TotalBdayMoney - 1;
            }
        }

        double MoneyFromToys = SingleToyPrice * ToyCount;
        double FinalRaisedMoney = TotalBdayMoney + MoneyFromToys;
        double Differance = Math.abs(FinalRaisedMoney - WashingMachinePrice);

        if (FinalRaisedMoney >= WashingMachinePrice){
            System.out.printf("Yes! %.2f\n", Differance );
        }
        else {
            System.out.printf("No! %.2f\n", Differance);
        }
    }
}
