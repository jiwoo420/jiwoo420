#include <stdio.h>

    int n,i,j;
    
    int x[100];
    int y[100];


int main()
{
   
    
    scanf("%d",&n); //n 입력 받는수
    
    for(i=0;i<n;i++){
        scanf("%d %d",&x[i],&y[i]);
        
        
    }
    
    for(i=0;i<n;i++){
        
        if(x[i]>x[i+1]){  // 정렬
            j=x[i];
            x[i]=x[i+1];
            x[i+1]=j;
        
            j=y[i];
            y[i]=y[i+1];
            y[i+1]=j;
            
            
            
        }
    
        if(x[i]==x[i+1] && y[i]>y[i+1]){     // 앞자리 같고 뒷자리 크면 뒤로 이동
            j=y[i];
            y[i]=y[i+1];                
            y[i+1]=j;
        }
        
        
        
    }
    
    for(i=0;i<n;i++){
        printf("%d %d\n",x[i],y[i]);
    
        
    }
    


    return 0;
}

