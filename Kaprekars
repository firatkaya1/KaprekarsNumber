import java.util.Scanner;

public class magicalNumber {

	public static void main(String[] args) {
		// Rastgele, rakamları birbirinden farklı 4 basamaklı bir sayi ele alalım.
				// örnek : 3765 --> büyükten kücüge rakamları sırala=7653 
				// --> küçükten büyüge sırala=3567  
				// Elde edilen iki sayidan birbirini çıkartalım. 7653-3567= 4086 
				// (büyükten kücüge)-(kücükten büyüge)=8640-0468=8172
				// (büyükten kücüge)-(kücükten-büyüge)=8721-1278=7443
				// (büyükten kücüge)-(kücükten-büyüge)=7443-3447=3996
				// (büyükten kücüge)-(kücükten-büyüge)=9963-3699=6264
				// (büyükten kücüge)-(kücükten-büyüge)=6642-2466=4176
				// (büyükten kücüge)-(kücükten-büyüge)=7641-1467=6174 
				
				// görüldüğü üzere en fazla 7 adımda hep aynı sonuca ulaşıldığı ortaya çıkmıştır. 
				// amaç, kullanıcının girdigi değeri adım adım hesaplayarak aynı sonuça ulaşmasını sağlamak. 
				
				
				Scanner in=new Scanner(System.in);
				System.out.println("Sihirli Sayiya ulaşmak için 4 haneli bir sayi giriniz:");
				int sayi=in.nextInt();
				
				if(control(sayi)) {
				System.out.println("Girdiginiz 4 haneli sayinin rakamları büyükten kücüge ve kücükten büyüge sıralanıyor..");
				for(int i=0;i<8;i++) {
					if(sayi!=6174) {
						System.out.println((i+1)+".adim "+buyuktenkucuge(sayi)+"-"+kucuktenbuyuge(sayi)+"="+sayi);
						sayi=buyuktenkucuge(sayi)-kucuktenbuyuge(sayi);
					
					}
					else {
						System.out.println((i+1)+".adim "+buyuktenkucuge(sayi)+"-"+kucuktenbuyuge(sayi)+"="+sayi);
						break;
					}
						
				} // for finisih

			}
				else {
					System.out.println("Lutfen rakamlar birbirinden farklı ve 4 basamaklı bir sayi giriniz.");
				}
				in.close();
			}
			
			
			public static boolean control(int sayi) {
				int A=sayi/1000;
				int B=(sayi/100)%10;
				int C=(sayi/10)%10;
				int D=(sayi%10);
				
				if(A!=B && A!=C && A!=D && B!=C && B!=D && C!=D && sayi<9999 && sayi>1000) {
					return true;
				}
				return false;

			}
			public static int buyuktenkucuge(int sayi) {
				// 4 haneli sayiyi buyukten kucuge sirala. // ABCD
				int A=sayi/1000;
				int B=(sayi/100)%10;
				int C=(sayi/10)%10;
				int D=(sayi%10);
				int dizi[]= {A,B,C,D};
				// 3765
				for(int i=0;i<dizi.length-1;i++) {
					int number=dizi[i];
					int temp=i;
						for(int j=i+1;j<dizi.length;j++) {
							if(dizi[j]>number) {
								number=dizi[j];
								temp=j;
								
							}
						}
						if(temp!=i) {
							
							dizi[temp]=dizi[i];
							dizi[i]=number;
						}

					}	// for bitiş
				String s=dizi[0]+""+dizi[1]+""+dizi[2]+""+dizi[3];
				sayi=Integer.valueOf(s);
				return sayi;
			}
			public static int kucuktenbuyuge(int sayi) {
				int A=sayi/1000;
				int B=(sayi/100)%10;
				int C=(sayi/10)%10;
				int D=(sayi%10);
				int dizi[]= {A,B,C,D};
				// 3765
				for(int i=0;i<dizi.length-1;i++) {
					int number=dizi[i];
					int temp=i;
						for(int j=i+1;j<dizi.length;j++) {
							if(dizi[j]<number) {
								number=dizi[j];
								temp=j;
								
							}
						}
						if(temp!=i) {
							
							dizi[temp]=dizi[i];
							dizi[i]=number;
						}

					}	// for bitiş
				String s=dizi[0]+""+dizi[1]+""+dizi[2]+""+dizi[3];
				sayi=Integer.valueOf(s);
				return sayi;
				
				}

	}
