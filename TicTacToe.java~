import java.util.Scanner;
import java.util.Random;
public class TicTacToe
{
  public static void main(String [] args)
  {
    Scanner x = new Scanner(System.in);
    Random rand = new Random();
    char player1_symbole;
    char player2_symbole;
    int user_choice;
    char array[][] = new char[3][3];
    int user = 0;
    
    for(;user == 0;)
    {
      System.out.println("1. Start game\n2. Instruction\n3. Credits\n4. Exit game");
      int user_command = x.nextInt();
      
      for(; (user_command < 1) || (user_command > 4);)
      {
        System.out.println("1. Start game\n2. Instruction\n3. Credits\n4. Exit game");
        user_command = x.nextInt();
      }
      
      if(user_command == 1)
      {
        System.out.println("1. Player VS computer\n2. Player VS Player");
        user_choice = x.nextInt();
        
        for(; (user_choice < 1) || (user_choice > 2);)
        {
          System.out.println("Invalid input");
          System.out.println("1. Player VS computer\n2. Player VS Player");
          user_choice = x.nextInt();
        }
        
        for(; user_command == 1;)
        {
          
//###############################################################################################################################################################################
                                                        //Player VS computer starts

          if(user_choice == 1)
          {
            int user_turn = rand.nextInt(2);
            
            for(int row = 0; row < 3; row++)
            {
              for(int collum = 0; collum < 3; collum++)
              {
                array[row][collum] = '_';
              }
            }
            if(user_turn % 2 == 0)
            {
              System.out.println("Player1's turn");
              System.out.println("Please select your symbole");
              System.out.println("1. O\n2. X ");
              int player1_input = x.nextInt();
              System.out.println(); 
              if(player1_input == 1)  //*************************************************** Player1's priority
              {
                player1_symbole = 'O';
                System.out.println("Player1, your symbole is " + player1_symbole);
                player2_symbole = 'X';
                System.out.println("Computer's your symbole is " + player2_symbole);
              }
              else
              {
                player1_symbole = 'X';
                System.out.println("Player1, your symbole is " + player1_symbole);
                player2_symbole = 'O';
                System.out.println("Computer's symbole is " + player2_symbole);
              }
            } 
            else         //****************************************************************** Computer's priority
            {
              int player2_input = rand.nextInt(2);
              System.out.println();
              
              if(player2_input == 1)
              {
                player2_symbole = 'O';
                System.out.println("Computer's symbole is " + player2_symbole);
                player1_symbole = 'X';
                System.out.println("Player1, your symbole is " + player1_symbole);
              }
              else
              {
                player2_symbole = 'X';
                System.out.println("Computer's symbole is " + player2_symbole);
                player1_symbole = 'O';
                System.out.println("Player1, your symbole is " + player1_symbole);
              }
            }
            
            //Symbole selection ends
//-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
//-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
            //Symbole placement Starts
            //******************player1's turn*********************
            
            int counter = 0;
            
            for(int turn = user_turn; turn < (user_turn + 9); turn ++)
            {
              if(turn % 2 == 0) //######################################################## Player1's turn
              {
                System.out.println();
                System.out.println("Player1's turn");
                System.out.println("   Please select a tile to place your symbole");
                System.out.println("      Please enter row number from 1 to 3");
                int row = x.nextInt();
                
                for(; (row < 1) || (row > 3);)
                {
                  System.out.println("Invalid input");
                  System.out.println("Please enter row number from 1 to 3");
                  row = x.nextInt();
                }
                
                System.out.println("      Please enter collum number from 1 to 3");
                int collum = x.nextInt();
                
                for(; (collum < 1) || (collum > 3);)
                {
                  System.out.println("Invalid input");
                  System.out.println("Please enter collum number from 1 to 3");
                  collum = x.nextInt();
                }
                
                for(; (array[row - 1][collum - 1] == player1_symbole) || (array[row - 1][collum - 1] == player2_symbole); )
                {
                  if((array[row - 1][collum - 1] == player2_symbole))
                  {
                    System.out.println("Player2 has already placed his symbole in this tile"); 
                  }
                  else
                  {
                    System.out.println("You have already placed yout symbole in this tile");  
                  }
                  
                  System.out.print("Please select another row and collum no out of 1 to 3 to place symbole");
                  System.out.println("      Please enter row number from 1 to 3");
                  row = x.nextInt() ;
                  
                  for(; (row < 1) || (row > 3);)
                  {
                    System.out.println("Invalid input");
                    System.out.println("Please enter row number from 1 to 3");
                    row = x.nextInt();
                  }
                  
                  System.out.println("      Please enter collum number from 1 to 3");
                  collum = x.nextInt();
                  
                  for(; (collum < 1) || (collum > 3);)
                  {
                    System.out.println("Invalid input");
                    System.out.println("Please enter collum number from 1 to 3");
                    collum = x.nextInt();
                  }
                }
                
                array[row - 1][collum - 1]= player1_symbole;
                System.out.println();
                
                for(int row1 = 0; row1 < 3; row1++)   
                {
                  for(int collum1 = 0; collum1 < 3; collum1++)
                  {
                    System.out.print(array[row1][collum1] + " ");
                  }
                  System.out.println();
                }
                System.out.println();
                
                //condition check
                
                if((array[0][0] == player1_symbole) && (array[0][1] == player1_symbole) && (array[0][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[1][0] == player1_symbole) && (array[1][1] == player1_symbole) && (array[1][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[2][0] == player1_symbole) && (array[2][1] == player1_symbole) && (array[2][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][0] == player1_symbole) && (array[1][0] == player1_symbole) && (array[2][0] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][1] == player1_symbole) && (array[1][1] == player1_symbole) && (array[2][1] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][2] == player1_symbole) && (array[1][2] == player1_symbole) && (array[2][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][0] == player1_symbole) && (array[1][1] == player1_symbole) && (array[2][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][2] == player1_symbole) && (array[1][1] == player1_symbole) && (array[2][0] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
              }
              
              //******************Computer's turn********************
              
              else //######################################################## Computer's turn
              {
                System.out.println();
                System.out.println("Computer's turn");
                int row = rand.nextInt(3);
                int collum = rand.nextInt(3);
                
                for(; (array[row ][collum ] == player1_symbole) || (array[row][collum] == player2_symbole);)
                {
                  row = rand.nextInt(3);
                  collum = rand.nextInt(3);
                }
                
                array[row][collum] = player2_symbole;
                System.out.println();
                
                for(int row1 = 0; row1 < 3; row1++)   
                {
                  for(int collum1 = 0; collum1 < 3; collum1++)
                  {
                    System.out.print(array[row1][collum1] + " ");
                  }
                  System.out.println();
                }
                System.out.println();
                
                //condition check
                
                if((array[0][0] == player2_symbole) && (array[0][1] == player2_symbole) && (array[0][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** COMPUTER IS THE WINNER ****************");
                  break;
                }
                else if ((array[1][0] == player2_symbole) && (array[1][1] == player2_symbole) && (array[1][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** COMPUTER IS THE WINNER ****************");
                  break;
                }
                else if ((array[2][0] == player2_symbole) && (array[2][1] == player2_symbole) && (array[2][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** COMPUTER IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][0] == player2_symbole) && (array[1][0] == player2_symbole) && (array[2][0] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** COMPUTER IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][1] == player2_symbole) && (array[1][1] == player2_symbole) && (array[2][1] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** COMPUTER THE WINNER ****************");
                  break;
                }
                else if ((array[0][2] == player2_symbole) && (array[1][2] == player2_symbole) && (array[2][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** COMPUTER IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][0] == player2_symbole) && (array[1][1] == player2_symbole) && (array[2][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** COMPUTER IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][2] == player2_symbole) && (array[1][1] == player2_symbole) && (array[2][0] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** COMPUTER IS THE WINNER ****************");
                  break;
                }
              }
            }
            if(counter == 9)
            {
              System.out.println("********************* GAME OVER *********************");
              System.out.println("************************ DRAW ************************");
            }
          }
         
          //                                                     Player VS computer ends
//###############################################################################################################################################################################
          
//###############################################################################################################################################################################
          //                                                     Player VS Player starts
          
          else 
          {
            int user_turn = rand.nextInt(2);
            
            for(int row = 0; row < 3; row++)
            {
              for(int collum = 0; collum < 3; collum++)
              {
                array[row][collum] = '_';
              }
            }
            
//-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
//-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
            //                                                   Symbole selection starts
            
            if(user_turn % 2 == 0)
            {
              System.out.println("Player1's turn");
              System.out.println("Please select your symbole");
              System.out.println("1. O\n2. X ");
              int player1_input = x.nextInt();
              System.out.println(); 
              if(player1_input == 1)  //*************************************************** Player1's priority
              {
                player1_symbole = 'O';
                System.out.println("Player1, your symbole is " + player1_symbole);
                player2_symbole = 'X';
                System.out.println("Player2, your symbole is " + player2_symbole);
              }
              else
              {
                player1_symbole = 'X';
                System.out.println("Player1, your symbole is " + player1_symbole);
                player2_symbole = 'O';
                System.out.println("Player2, your symbole is " + player2_symbole);
              }
            } 
            else         //****************************************************************** Player2's priority
            {
              System.out.println("Player2's turn");
              System.out.println("Please select your symbole");
              System.out.println("1. O\n2. X ");
              int player2_input = x.nextInt();
              System.out.println();
              
              if(player2_input == 1)
              {
                player2_symbole = 'O';
                System.out.println("Player2, your symbole is " + player2_symbole);
                player1_symbole = 'X';
                System.out.println("Player1, your symbole is " + player1_symbole);
              }
              else
              {
                player2_symbole = 'X';
                System.out.println("Player2, your symbole is " + player2_symbole);
                player1_symbole = 'O';
                System.out.println("Player1, your symbole is " + player1_symbole);
              }
            }
            
            //                                        Symbole selection ends
//-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
//-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
            //                                        Symbole placement Starts
            //                           ******************player1's turn*********************
            
            int counter = 0;
            
            for(int turn = user_turn; turn < (user_turn + 9); turn ++)
            {
              if(turn % 2 == 0) //######################################################## Player1's turn
              {
                System.out.println();
                System.out.println("Player1's turn");
                System.out.println("   Please select a tile to place your symbole");
                System.out.println("      Please enter row number from 1 to 3");
                int row = x.nextInt();
                
                for(; (row < 1) || (row > 3);)
                {
                  System.out.println("Invalid input");
                  System.out.println("Please enter row number from 1 to 3");
                  row = x.nextInt();
                }
                
                System.out.println("      Please enter collum number from 1 to 3");
                int collum = x.nextInt();
                
                for(; (collum < 1) || (collum > 3);)
                {
                  System.out.println("Invalid input");
                  System.out.println("Please enter collum number from 1 to 3");
                  collum = x.nextInt();
                }
                
                for(; (array[row - 1][collum - 1] == player1_symbole) || (array[row - 1][collum - 1] == player2_symbole); )
                {
                  if((array[row - 1][collum - 1] == player2_symbole))
                  {
                    System.out.println("Player2 has already placed his symbole in this tile"); 
                  }
                  else
                  {
                    System.out.println("You have already placed yout symbole in this tile");  
                  }
                  
                  System.out.print("Please select another row and collum no out of 1 to 3 to place symbole");
                  System.out.println("      Please enter row number from 1 to 3");
                  row = x.nextInt() ;
                  
                  for(; (row < 1) || (row > 3);)
                  {
                    System.out.println("Invalid input");
                    System.out.println("Please enter row number from 1 to 3");
                    row = x.nextInt();
                  }
                  
                  System.out.println("      Please enter collum number from 1 to 3");
                  collum = x.nextInt();
                  
                  for(; (collum < 1) || (collum > 3);)
                  {
                    System.out.println("Invalid input");
                    System.out.println("Please enter collum number from 1 to 3");
                    collum = x.nextInt();
                  }
                }
                
                array[row - 1][collum - 1]= player1_symbole;
                System.out.println();
                
                for(int row1 = 0; row1 < 3; row1++)   
                {
                  for(int collum1 = 0; collum1 < 3; collum1++)
                  {
                    System.out.print(array[row1][collum1] + " ");
                  }
                  System.out.println();
                }
                System.out.println();
                
                //condition check
                
                if((array[0][0] == player1_symbole) && (array[0][1] == player1_symbole) && (array[0][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[1][0] == player1_symbole) && (array[1][1] == player1_symbole) && (array[1][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[2][0] == player1_symbole) && (array[2][1] == player1_symbole) && (array[2][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][0] == player1_symbole) && (array[1][0] == player1_symbole) && (array[2][0] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][1] == player1_symbole) && (array[1][1] == player1_symbole) && (array[2][1] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][2] == player1_symbole) && (array[1][2] == player1_symbole) && (array[2][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][0] == player1_symbole) && (array[1][1] == player1_symbole) && (array[2][2] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][2] == player1_symbole) && (array[1][1] == player1_symbole) && (array[2][0] == player1_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER1 IS THE WINNER ****************");
                  break;
                }
              }
              
              //******************player1's turn********************
              
              else //######################################################## Player2's turn
              {
                System.out.println();
                System.out.println("Player2's turn");
                System.out.println("   Please select a tile to place your symbole");
                System.out.println("      Please enter row number from 1 to 3");
                int row = x.nextInt() ;
                for(; (row < 1) || (row > 3);)
                {
                  System.out.println("Invalid input");
                  System.out.println("Please enter row number from 1 to 3");
                  row = x.nextInt();
                }
                System.out.println("      Please enter collum number from 1 to 3");
                int collum = x.nextInt();
                for(; (collum < 1) || (collum > 3);)
                {
                  System.out.println("Invalid input");
                  System.out.println("Please enter collum number from 1 to 3");
                  collum = x.nextInt();
                }
                
                for(; (array[row - 1][collum - 1] == player1_symbole) || (array[row - 1][collum - 1] == player2_symbole);)
                {
                  if((array[row - 1][collum - 1] == player1_symbole))
                  {
                    System.out.println("Player1 has already placed his symbole in this tile"); 
                  }
                  else
                  {
                    System.out.println("You have already placed yout symbole in this tile");  
                  }
                  
                  System.out.print("Please select another row and collum no out of 1 to 3 to place symbole");
                  System.out.println("      Please enter row number from 1 to 3");
                  row = x.nextInt() ;
                  
                  for(; (row < 1) || (row > 3);)
                  {
                    System.out.println("Invalid input");
                    System.out.println("Please enter row number from 1 to 3");
                    row = x.nextInt();
                  }
                  
                  System.out.println("      Please enter collum number from 1 to 3");
                  collum = x.nextInt();
                  
                  for(; (collum < 1) || (collum > 3);)
                  {
                    System.out.println("Invalid input");
                    System.out.println("Please enter collum number from 1 to 3");
                    collum = x.nextInt();
                  }
                }
                
                array[row - 1][collum - 1] = player2_symbole;
                System.out.println();
                
                for(int row1 = 0; row1 < 3; row1++)   
                {
                  for(int collum1 = 0; collum1 < 3; collum1++)
                  {
                    System.out.print(array[row1][collum1] + " ");
                  }
                  System.out.println();
                }
                System.out.println();
                
                //condition check
                
                if((array[0][0] == player2_symbole) && (array[0][1] == player2_symbole) && (array[0][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER2 IS THE WINNER ****************");
                  break;
                }
                else if ((array[1][0] == player2_symbole) && (array[1][1] == player2_symbole) && (array[1][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER2 IS THE WINNER ****************");
                  break;
                }
                else if ((array[2][0] == player2_symbole) && (array[2][1] == player2_symbole) && (array[2][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER2 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][0] == player2_symbole) && (array[1][0] == player2_symbole) && (array[2][0] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER2 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][1] == player2_symbole) && (array[1][1] == player2_symbole) && (array[2][1] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER2 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][2] == player2_symbole) && (array[1][2] == player2_symbole) && (array[2][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER2 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][0] == player2_symbole) && (array[1][1] == player2_symbole) && (array[2][2] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER2 IS THE WINNER ****************");
                  break;
                }
                else if ((array[0][2] == player2_symbole) && (array[1][1] == player2_symbole) && (array[2][0] == player2_symbole))
                {
                  System.out.println("**************** GAME OVER ****************");
                  System.out.println("**************** PLAYER2 IS THE WINNER ****************");
                  break;
                }
              }
              counter++;
            }
            
            if(counter == 9)
            {
              System.out.println("********************* GAME OVER *********************");
              System.out.println("************************ DRAW ************************");
            }
            
            //Player VS Player ends
//###############################################################################################################################################################################
          }
          
          System.out.println();
          System.out.println("1. Replay\n2. Main Menu\n3. Exit game");
          int user_command2 = x.nextInt();
          System.out.println();
          
          for(; (user_command2 < 1) || (user_command2 > 3);)
          {
            System.out.println("Wrong input");
            System.out.println("1. Replay\n2. Main Menu\n3. Exit game");
            user_command2 = x.nextInt();
          }
          
          if(user_command2 == 1)
          {
            user_command = 1;
          }
          else if(user_command2 == 2)
          {
            break;
          }
          else if(user_command2 == 3)
          {
            user = 1;
            break;
          }
        }
      }
      else if(user_command == 2)
      {
        System.out.println();
        System.out.println("Tic-Tac-Toe is played on a 3X3 board between 2 players.\nThe objective of this game is to try and conquer the board.\nTo conquer the board one has to align his 3 symbols in a row or column or diagonal.\nBetween the two players, the player who is able to conquer the board before the other player is the winner.\nIf none of the players are able to conquer the board within the last turn of the game, which is 9th turn, is over then the game is considered as a draw.\n");
        System.out.println();
        System.out.println("Turn fact:\n");
        System.out.println("   To make this game a little bit interesting and a little bit more fair, which player will go first will be decided randomly.\n   Now, everyone has the same probability for starting at first.\n");
        System.out.println(3);
        System.out.println("1. Main menu\n2. Exit game");
        int command = x.nextInt();
        
        for(; (command < 1) || (command > 2);)
        {
          System.out.println("Wrong input");
          System.out.println("1. Main menu\n2. Exit game");
          command = x.nextInt();
        }
        if(command == 2)
        {
          break;
        }
      }
      else if(user_command == 3)
      {
        System.out.println();
        System.out.println("This game was developed by\n K.M. Abdullah Al Maruf\n ID: 19101487 \n Department: CSE \n (Semester - Spring-2019, Brac University)\n");
        System.out.println("1. Main menu\n2. Exit game");
        int command = x.nextInt();
        
        for(; (command < 1) || (command > 2);)
        {
          System.out.println("Wrong input");
          System.out.println("1. Main menu\n2. Exit game");
          command = x.nextInt();
        }
        if(command == 2)
        {
          break;
        }
      }
      else if(user_command == 4)
      {
        break;
      }
    }
  }
}