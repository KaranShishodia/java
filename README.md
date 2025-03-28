Tic Tac Toe
game build to play.
easy prooject .Tic Tac Toe is a simple and classic two-player game. The game is played on a 3x3 grid. Players take turns marking a space in the grid with their symbol: either an "X" or an "O". The goal is to be the first player to get three of your symbols in a row—horizontally, vertically, or diagonally.
Here are the key points:

It's great for quick, strategic fun! If you'd like, I can guide you in coding a simple Tic Tac Toe game in Java. Let me know if you're up for the challenge.

import java.util.Scanner;

        char player = 'X';
        boolean gameOver = false;
        Scanner sc = new Scanner(System.in);
        while(!gameOver){
            printBoard(board);
            System.out.println("Player"+player="enter:");
            int row = sc.nextInt();
            int col = sc.nextInt();

            if(board[row][col] = ' '){
                board[row][col] = player;
                gameOver = haveWon(board,player);
                if(gameOver){
                    System.out.println("Player"+player="has won:");
                }
            else {
                player = (player == 'X') ? 'o' : 'X';
                }
            }
            else {
                System.out.println("Invalid move. Try again");
            }
        }
        printBoard(board);
    }
     public static boolean haveWon(char[][] board,char player){
        for(int row = 0;row<board.length;row++){
            if(board[row][0] == player && board[row][1] == player && board[row][2] == player){
                return true;
            }
        }
         for(int col = 0;col<board[0].length;row++){
            if(board[0][col] == player && board[1][col] == player && board[2][col] == player){
                return true;
            }
        }
        if(board[0][0] == player && board[1][1] == player && board[2][2] == player){
            return true;
        }
        if(board[0][2] == player && board[1][1] == player && board[2][0] == player){
            return true;
        }
        return false

     }
    public static void printBoard(char[][] board){
        for(int row = 0;row<board.length;row++){
            for(int col=0;col<board[row].length;col++){
                System.out.print(board[row][col] + " | ");
            }
            System.out.println( );
        }
        public class tictactoe{
    public static void main(){
        char[][] board = new char[3][3];
        for(int row = 0;row<board.length;row++){
            for(int col=0;col<board[row].length;col++){
                board[row][col] = ' ';

            }
        }
    }
}
        
