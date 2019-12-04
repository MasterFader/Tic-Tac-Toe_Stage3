package tictactoe;
//import java.util.Arrays;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        String inputString = scanner.nextLine();
        int counter9 = 0;
        char[][] matrix = new char[3][3];

        int xCount = 0;
        int oCount = 0;
        int blankCount = 0;

        boolean xWins = false;
        boolean oWins = false;
        boolean emptyCells = false;
        boolean gameNotFinished = false;
        boolean impossible = false;

        // 'X' 'O' '_' counter
        for(int i=0;i<9;i++){
            if(inputString.charAt(i) == '_'){
                blankCount++;
            }else if(inputString.charAt(i) == 'O'){
                oCount++;
            }else if(inputString.charAt(i) == 'X'){
                xCount++;
            }
        }

//        // Impossible scenario check
//        if(xCount-oCount>=2){
//            impossible = true;
//        }else if (oCount-xCount>=2){
//            impossible = true;
//        }

        if(blankCount>0){
            emptyCells = true;
        }
        //filling the 2D Matrix
        tictactoeFillingMatrix(inputString, counter9, matrix);

        // Check diagonals + check X axis + check Y axis for both 'X' 'O'
        if(matrix[0][0] == 'X' && matrix[0][0] == matrix[1][1] &&  matrix[1][1] == matrix[2][2] ){
            xWins = true;
        }else if(matrix[0][2] == 'X' && matrix[0][2] == matrix[1][1] &&  matrix[1][1] == matrix[2][0]){
            xWins = true;
        }

        if(matrix[0][0] == 'O' && matrix[0][0] == matrix[1][1] &&  matrix[1][1] == matrix[2][2] ){
            oWins = true;
        }else if(matrix[0][2] == 'O' && matrix[0][2] == matrix[1][1] &&  matrix[1][1] == matrix[2][0]){
            oWins = true;
        }

        for(int i=0;i<matrix.length;i++){
            int counterX = 0;
            int counterO = 0;
            for(int j=0;j<matrix.length;j++){
                if(matrix[i][j] == 'X'){
                    counterX++;
                    counterO = 0;
                }else if(matrix[i][j] == 'O'){
                    counterO++;
                    counterX = 0;
                }
                if(counterX == 3){
                    xWins = true;
//                    System.out.println("X wins");
                }else if(counterO == 3){
                    oWins = true;
//                    System.out.println("O wins");
                }
            }
        }

        for(int i=0;i<matrix.length;i++){
            int counterX = 0;
            int counterO = 0;
            for(int j=0;j<matrix.length;j++){
                if(matrix[j][i] == 'X'){
                    counterX++;
                    counterO = 0;
                }else if(matrix[j][i] == 'O'){
                    counterO++;
                    counterX = 0;
                }
                if(counterX == 3){
                    xWins = true;
//                    System.out.println("X wins");
                }else if(counterO == 3){
                    oWins = true;
//                    System.out.println("O wins");
                }
            }
        }

        if(xWins&&oWins){
            impossible = true;
            System.out.println("Impossible");
        }
        if(xCount-oCount>=2){
            impossible = true;
        }else if (oCount-xCount>=2){
            impossible = true;
        }
        if(xWins && !impossible){
            System.out.println("X wins");
        }else if(oWins && !impossible){
            System.out.println("O wins");
        }else if(xCount-oCount>=2){
//            impossible = true;
            System.out.println("Impossible");
        }else if (oCount-xCount>=2){
//            impossible = true;
            System.out.println("Impossible");
        }else if(!xWins && !oWins && emptyCells){
            System.out.println("Game not finished");
        }else if(!xWins && !oWins){
            System.out.println("Draw");
        }

    }

    private static void tictactoeFillingMatrix(String inputString, int counter9, char[][] matrix) {
        for (int i = 0; i < matrix.length; i++) {
            for (int j = 0; j < matrix.length; j++) {
                matrix[i][j] = inputString.charAt(counter9 + j);
            }
            counter9 += 3;
        }
    }
}
