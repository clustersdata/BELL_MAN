# BELL_MAN

BELL_MAN

inline void init(int d[M],int n,int s){  //初始化图

	int i;
  
	for(i=1;i<=n;i++)	d[i]=2000000000;
  
	d[s]=0;
  
}


inline void relax(int d[M],int u,int v,int duv){

	if(d[v]>d[u]+duv)	d[v]=d[u]+duv;
  
}


void bell_man(int g[M][M],int d[M],int n,int s){ //n个结点 s为源点

	int i,j,k;
  
	init(d,n,s);
  
	for(k=1;k<n;k++){
  
		for(i=1;i<=n;i++)
    
    
			for(j=1;j<=n;j++){
      
				if(g[i][j]!=0) relax(d,i,j,g[i][j]);
        
			}
      
	}
  
}
