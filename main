#include <stdio.h>

int WhereYouCanPut(int chessboard[8][8], int x, int y, int dx, int dy){
  int mine = chessboard[x][y];
  int opponent = 3 - chessboard[x][y];
  int count = 0;
  if (mine != EMPTY){ 
  
    //check 左上  
    if (dx == -1 && dy == -1){
      while (chessboard[x-dx][y-dy] == opponent){
        dx++;
        dy++;
        if (chessboard[x-dx][y-dy] == EMPTY){
          printf("(%d, %d)\n", x-dx, y-dy);
          count++;
          break;
        }
      }
    }
      
   //check 右上
   else if(dx ==1 && dy == -1){
     while (chessboard[x+dx][y-dy] == opponent){
       dx++;
       dy++;
       if (chessboard[x+dx][y-dy] == EMPTY){
         printf("(%d, %d)\n", x+dx, y-dy);
         count++;
         break;
       }
     }
   }
    //check 右下
    else if (dx == 1 && dy == 1){
      while (chessboard[x+dx][y+dy] == opponent){
        dx++;
        dy++;
        if (chessboard[x+dx][y+dy] == EMPTY){
          printf("(%d, %d)\n", x+dx, y+dy);
          count++;
          break;
        }
      }  
    }

    else if (dx == 0 && dy == -1){
      //check 上方
      while (chessboard[x][y-dy] == opponent){
        dy++;
        if (chessboard[x][y-dy] == EMPTY){
          printf("(%d, %d)\n", x, y-dy);
          count++;
          break;
        }
      }
    }
    
    //check 下方
    else if (dx == 0 && dy == 1){
      while (chessboard[x][y+dy] == opponent){
        dy++;
        if (chessboard[x][y+dy] == EMPTY){
          printf("(%d, %d)\n", x, y+dy);
          count++;
          break;
        }
      }
    }
    //check 左
    else if (dx == -1 && dy == 0){
      while (chessboard[x-dx][y] == opponent){
        dx++;
        if (chessboard[x-dx][y] == EMPTY){
          printf("(%d, %d)\n", x-dx, y);
          count++;
          break;
        }
      }
    }
    
    //check 右
    else{
      while (chessboard[x+dx][y] == opponent){
        dx++;
        if (chessboard[x+dx][y] == EMPTY){
          printf("(%d, %d)\n", x+dx, y);
          count++;
          break;
        }
      }
    }
  } //the end of if
  
  else printf("you put a blank chess.\n");
  
  printf("%d", count);
  return 0;
}


//main code
int main() {
  int i, j, x, y, dx, dy, result;
  int chessboard[8][8] = {0};
  //input chessboard
  for (j=0; j<8; j++){
    for (i=0; i<8; i++){
      scanf("%d", &chessboard[i][j]);
    }
  }  
  
  scanf("%d%d%d%d", &x, &y, &dx, &dy);
  result = WhereYouCanPut(chessboard[8][8], x, y, dx, dy);
  //printf("%d", result);
  
  



  return 0;
}

// end of main
