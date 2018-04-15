#include<stdio.h>
#include<stdlib.h>
typedef struct{
int jour , mois , annee ;
}date;
main(){
	system ("color 3f");
	char nom[10], prenom[10];
	int r=1;
	date da , dn , age ;
	printf("Bonjour !!\n");
	printf("donner la date d'aujourd'hui : \nLe jour : ");scanf("%d",&da.jour);while((da.jour<1) or (da.jour>31)){scanf("%d",&da.jour);}
	printf("Le mois : ");scanf("%d",&da.mois);while((da.mois<1) or (da.mois>12)){scanf("%d",&da.mois);}
	printf("L'annee : ");scanf("%d",&da.annee);	
	while (r=1){
	printf("Donner le nom : "); scanf("%s",&nom);
	printf("Donner le prenom : "); scanf("%s",&prenom);
	printf("donner la date de naissance : \nLe jour : ");scanf("%d",&dn.jour);while((dn.jour<1) or (dn.jour>31)){scanf("%d",&dn.jour);}
	printf("Le mois : ");scanf("%d",&dn.mois);while((dn.mois<1) or (dn.mois>12)){scanf("%d",&dn.mois);}
	printf("L'annee : ");scanf("%d",&dn.annee);while(dn.annee>da.annee){scanf("%d",&dn.annee);}
	if (da.mois<dn.mois) {age.annee=da.annee-dn.annee-1;
	   if (da.jour<dn.jour){age.mois=12-(dn.mois-da.mois)-1;age.jour=30-(dn.jour-da.jour);}
	      else{age.mois=12-(dn.mois-da.mois);age.jour=da.jour-dn.jour;}}
	   else { if (da.jour<dn.jour) {age.annee=da.annee-dn.annee-1;age.mois=12-(dn.mois-da.mois)-1;age.jour=30-(dn.jour-da.jour);} 
	             else {age.annee=da.annee-dn.annee;age.mois=(da.mois-dn.mois);age.jour=da.jour-dn.jour;} }
    printf("\n\nLe nom : %s\nLe prenom : %s\nL'age est : %d ans , %d mois et %d jours .. \n",nom,prenom,age.annee,age.mois,age.jour);
	printf("L'age au total : %d jours \n\n",(age.annee*365)+(age.mois*30)+age.jour);
    printf("entrer '1' si vous voulais calculer un autre age : ");
	scanf("%d",&r);
}
return 0 ;
}
