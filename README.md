# atcoder-B ABC083
atcoderの過去問
//使用言語　C
#include<stdio.h>
int main(){
  int N;
  scanf("%d",&N);
  int point[N],a;
  for(a=0;a<N;a++){
    scanf("%d",&point[a]);
  }//入力
  int b;
  for(a=0;a<N;++a){//バブルソート  最初が大きければいい
    for(b=a+1;b<N;++b){
      if(point[a]<point[b]){
        int tmp=0;
        tmp = point[b];
        point[b]=point[a];
        point[a]=tmp;//入れ替え
      }
    }//最初のpoint[0]
  }
  int Alice=0,Bob=0;
  for(a=0;a<N;a++){
    if(a%2==0){
      Alice+=point[a];
    }
    else{
      Bob+=point[a];
    }
  }
  printf("%d",Alice-Bob);
  
  
  
}
