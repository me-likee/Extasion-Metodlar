# Extasion-Metodlar
//3^4 işlemini yapmak için 
int result=1;
for (int i = 1; i < 5; i++)
    result=result*3;
Console.WriteLine(result);

İslemler instance=new();
Console.WriteLine(instance.Expo(3,4));

string metin="Melike Tutkun ";
bool sonuc=metin.Checkspace();
Console.WriteLine(sonuc);
if(sonuc)
{
    Console.WriteLine(metin.RemoteWhiteSpace());

}
Console.WriteLine(metin.MakeUpperCase());
Console.WriteLine(metin.MakeLowerCase());

int[] dizi={1,9,6,5,4,7};
dizi.SortArray();
dizi.EkranaYazdir();
int sayi=5;
Console.WriteLine(sayi.IsEvenNumber());
Console.WriteLine(metin.firstcharackter());
public class İslemler{
    
    public int Expo(int sayi,int üs)
    {
        if(üs<2)
            return sayi;
        return Expo(sayi,üs-1)*sayi;
        //Expo(3,4)
        //Expo(3,3)*3
        //Expo(3,2)*3*3
        //Expo(3,1)*3*3*3
        //3*3*3*3=3^4
    }
}
public static class Extansion{

    public static bool Checkspace(this string param)//metinde boşluk varsa true yoksa false dönen extansion metod
    {
        return param.Contains(" ");
    }
    public static string RemoteWhiteSpace(this string param)
    {
       string[] dizi=param.Split("git branch -M main");//Yazıyı boşluk ifadesinden ayır ve bir diziye ata
       return string.Join("",dizi); // Ardından bu dizideki boşluk yerine"" ile birleştir yani boşluksuz yazıcak
    }
    public static string MakeUpperCase(this string param)// Yazıyı Büyük harf ile yazar
    {
        return param.ToUpper();
    }
    public static string MakeLowerCase(this string param)// Yazıyı küçük harf ile yazar
    {
        return param.ToLower();
    }
     public static int[] SortArray(this int[] param)// diziyi sıralar
    {
        Array.Sort(param);
        return param;
    }
     public static void EkranaYazdir(this int[] param)
    {
        foreach (var item in param)
        {
            Console.WriteLine(item);   
        }
     
    }
      public static bool IsEvenNumber(this int param)
    {
       return param%2==0;
     
    }
      public static string firstcharackter(this  string param )
    {
       return param.Substring(0,1);//0dan başlayıp uzunluğunu veriyoruz biz ilk karakteri almak istedik
     
    }
}
