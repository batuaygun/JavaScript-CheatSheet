# Değişkenler(Variables)
### Değişken tanımlama kuralları


1.değişken isimleri rakam ile başlayamaz. yas1 olur 1yas olmaz

2. If, For gibi komutları değişken olarak belirtemeyiz.

3. değişken adı verirken arada boşluk bırakılamaz. alt tire _ yada camelCase olabilir.

4. Değişken isimlerinde türkçe karakter kullanılmamalıdır.

#### Değişken Türleri ikiye ayrılır

    1. **Primitive Types**
          String 
            var, let

       let firstname="Batu";
       
>değişken türünü anlamak için console.log(typeof firstName)
>String çıktısı olur

**Number** 

    let age= 30;
      console.log(typeof age); 
      
>number çıktısı olur.

**Boolean**

     let kredi_kullanimi=false
      console.log(typeof false)
        
>boolean çıktısı olur

**Undefined**

    let phone;
      console.log(typeof phone)
>undefined çıktısı olur.


2. Reference types

**Objects**

   Array
   
    let liste=["aslı", "kerem","batu"]
      console.log(typeof liste)
>object çıktısı olur

**Objects Literals**

      let address={
          city:"istanbul",
           country:"Türkiye" }
            console.log(typeof address)
>object olarak çıkar.

            var hesapla=function(){
                return 0;}
                  console.log(typeof hesapla)
>function çıktısı olur.

***********************************************************
### OPERATÖRLER

1. Aritmetik Operatrler
      let veri;
       const a=20;
       const b=10; 
       let d=3;
       const c=5;

          veri=a+b;
            veri=a-b;
              veri=a*b;
              
              veri=a/b;
                veri=d++;    //Bir artırmak için a+1 de olabilir.
                    veri=a%b;    //bu a nın b ye bölümünden kalandır.

 ****************************************************************
 
2. Atama Operatörleri

            veri = a;
              veri +=a;   //şöyle ki bu veri= veri+a demek
              veri -=a;    //şöyle ki veri= veri-a demek
                veri %=a;     şöyle ki veri=veri % a; 
                >sayı tek mi çift mi hesabında kullanılır çünkü çift ise 0 tek ise 1 çıkar.

 ****************************************************************

3. Karşılaştırma Operatörleri

      veri = a==b;   boolean false
          veri = b==c;   boolean false

          veri= 5==="5"; //bu ise hem tür hem değer olarak eşit olmalıdır. String numbera eşit değildir.
              veri= a!=b; //eşit değildir sonucudur.

                veri= a>b    boolean true
                  veri= b<c    boolean false    
 ****************************************************************

4. Mantıksal Operatörler

      && (and)
        veri=(a>b) &&(a>c)  //true çıkar çünkü iki değer de doğrudur.

         || (veya) 
          veri= (b>a) || (a>c)   //true çıkar çünkü bir değer doğru

            ! not demektir
              veri =!(a>b) //true olmasına rağmen false cevabını verir değil işareti cevabı değiştirir.




 ****************************************************************

### DATE OBJECT
    

        let zaman= new Date();
        let birthday=new Date(1994,10,17);
        console.log(zaman);
        console.log(typeof zaman);

**Get Methods (Zamanın anlık durumu neyse odur.)**

        console.log(zaman.getMonth());
          console.log(zaman.getDate());


**Set Methods (Zamanı kendimiz değiştirmek için.)**

    zaman.setDate(25);
      zaman.setMonth(3);
        zaman.setFullYear(2024);
          zaman.setHours(20);



console.log(zaman.getFullYear()-birtday.getFullYear);

 ****************************************************************

### Numbers

        let veri;

      veri= Number("5");   // 5 sonucunu verir direkt number olarak alır
        veri= parseInt("5");// 5 sonucunu verir direkt
        
       veri= parseFloat("5.5"); //5.5 sonucunu verir
        veri= parseInt("5c"); //5 sonucunu verir
        
       veri= parseInt("c5");// NaN not a number sonucu çıkar
         veri= isNaN("c5"); //veri bir not a number mıdır? EVET sonucu çıkar true çünkü sayı değildir.
          veri= isNaN("5"); //veri bir not a number mıdır? Hayır sonucu çıkar çünkü sayıdır False

        var sayi=15.3242354234;
          veri = sayi.toPrecision(3); // soldan itibaren 3 basamak verir.
            veri=sayi.toFixed(3); // virgülden sonra 3 basamak gösterir.

         veri= Math.PI;
          veri=Math.round(3.5); // yuvarlama işlemi var
          
          veri= Math.ceil(3.2); // her zaman yukarı yuvarlar
           veri= Math.floor(8.3); // her zaman aşağıya yuvarlar.
           
          veri=Math.pow(3,3);   // 3 üssü 3 olur 27 sonucu çıkar.
           veri= Math.sqrt(81); // Karekök işlemidir 9 sonucu çıkar.
           
          veri=Math.abs(-50);   // Mutlak değer işlemidir.
            veri=Math.min(3,2,6,5,4,8,6,); // değerler arasındaki en düşük değeri alır.
            
          veri=Math.max(3,2,6,5,4,8,6,); // değerler arasındaki en büyük değeri alır.
            veri=Math.random(); // bu şekilde 0 ile 1 arasında bir sayı üretir
            
          veri=Math.random()*10 // 0 ile 10 arasında üretir.
            veri=Math.floor(Math.random()*10); // böyle olursa ondalıklı kısmı almaz aşağıya yuvarlar.
            
              console.log(veri);
                console.log(typeof veri);


 ****************************************************************
 


### STRINGS


        const firstname="Batu";
          const lastname="Aygün";
            const age= "29";
              let hobbies="f1 sinema kitap yazılım"

        let veri;

    string birleştirme(String concatenations)
      veri= firstname+" "+lastname;
      
        veri="Batu";
          veri+=" Aygün"; 
            veri ='Merhabalar '+firstname+' '+lastname+' Benim Adım'+' '+ 'Yaşım '+age+ ' ve İstanbul\'da yaşıyorum';
              veri= firstname.concat(' ',lastname);  // Diğer bir method


       veri= veri.toUpperCase();
          veri=veri.toLowerCase();
            veri= veri.substring(3,7); // 3 ile 7 arasında ki indeksi alır.
            
        veri=veri.slice(1,8); // 1 i almaz 8 i almaz arasındaki tüm hargleri alır.
          veri= veri.indexOf("t"); // t harfi kaçıncı indekste bulunmaktadır. Eğer ki içerisinde olmayan karakter varsa -1 sonucu çıkar
            veri=veri.replace("BATU","Batuhan");
>veri de isim olarak Batu yazdım ama kodların içinde to upper case komutuyla ben Batuyu BATU ya çevirdim bundan dolayı BATU olarak yapmak durumunda kaldım.
        veri=veri.length;
           veri=hobbies.split(' ');

          console.log(veri);
            console.log(typeof veri);
