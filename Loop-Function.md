#                           **BATUHAN AYGÜN JAVASCRIPT CHEAT SHEET VOL.3**

## **Döngüler (LOOPS)**


 >3 döngü tipi vardır (1-While 2-Do while 3-For döngüsüdür.

### 1. **While loop**

     let i= 0;
      while (i<10){ 
      >sonsuz döngüdür. i nin değeri 0 ve döngünün koşulu 10dan küçük olmalı haliyle bu döngü sürekli çalışacağı için 0 dır.
          console.log(i);
          }


          let i=0; // birer birer artar ve 10 olduğunda döngü biter
          while(i<10){
           console.log(i);
            i+=1; //i++; kullanılabilir.
              }


          let x=10;
           while(i>0){
            console.log(i);
              i--;
                 }


            break ve continue komutu
              let a = 0;
                 while (a < 10) {
                    console.log(a);
                     if (a == 6) {
                        break; // Döngü belirlenen noktaya geldiği anda durur.
                          }
                             a++;
                               }

 >continue çalışma mantığı şöyle ki statement içindeki belirtilen o noktayı atlar ve döngüyü işlemeye devam eder. 
 >Ufak bir ipucu Continue komutunu if döngüsünde kullan daha iyi



-------------------------------------------------------------

### 2. **Do-while**

>normal while döngüsünden farkı olarak öncelikle do döngüsünü çalıştırıyor daha sonra while koşuluna bakıyor.
>Eğer koşul devam ediyorsa yukarı çıkıp döngüyü çalıştırmaya devam ediyor.
>normal while da ise önce koşula bakıyor eğer koşul çalışıyorsa altındaki komutları çalıştırıyor. 
>Do-While da ise önce bir çalıştırıyor sonra koşula bakıyor. Koşul çalıştıkça döngü devam ediyor.

          let i= 0;
            do{
            console.log(i);
              i++;
                }while(i<10);

-------------------------------------------------------------------
### 3. **FOR** 

      for(let i=0; i<10; i++){
          console.log(i);
            }


         for(let i=0; i<10; i++){
             if(i==3){
              console.log("Seçilen Rakam: "+i); 
                >şöyle ki continue dediğimizde 3 ü atlayıp döngüye devam etmesi lazımdı ama 
                >console.log ile biz aslında orda bir gösterim sağladık. 
         
         continue; 
           >burda break; komutu kullansaydık döngüyü 3 te kıracaktı ve devamı gelmeyecekti
              }
               console.log(i);
                  }



          let toplam=0;
            for(let i=1; i<10; i++){
               toplam=toplam+i;  // böyle uzun uzun göstermek yerine toplam+=i; komutu da kullanılabilir.
                       }
                      console.log(toplam);


                  let carpma=1; // 1 dememizin sebebi 0 çarpmada yutan eleman
                    for(let a=1; a<10; a++){
                        carpma*=a;
                            }
                            console.log(carpma);




***********************************************************************************
***********************************************************************************
***********************************************************************************


## **Dizi ve objelerde döngü kullanımı** 


      let citys=["İstanbul","Ankara","İzmir","Bursa"];
        let users=[
          {firstName:"Aslı", lastName:"Yılmaz"},
          {firstName:"Batuhan", lastName:"Aygün"},
          {firstName:"Alperen", lastName:"Yeşiltaş"},
          {firstName:"Çiğdem", lastName:"Aygün"},]
##### Arrays

      for(let i=0;i<citys.length; i++){
    console.log(citys[i]); 
    >[i] bu şekilde kullanmamızın sebebi dizi içerisindeki öğelerin for döngüsü ile birlikte artarken teker teker ekrana yazılmasıdır. 
    >kullanılmazsa eğer dizi uzunluğu kadar örnek olarak 5 kez aynı diziyi yazdırır.
}



##### for-in metodu

     for(let i in citys){
    console.log(`index:${i} value: ${citys[i]}`); 
    >Bu işlemin yapılabilmesi için option+virgül kullanarak özel tırnak oluşturulur. Stringleri birleştirme işlevi görür.
}

##### For Each Methodu

    citys.forEach(function(item){    
    > İtem dizi içerisindeki elemanları kendi içerisine kopyalıyor.
      console.log(item);
      }); 
> yukardaki normal for döngüsü ile yaptığımız işlemin aynısı ama daha pratik.


      for(let i=0; i<users.length; i++){
        console.log(users[i].firstName);  
        >obje içerisindeki elemanların firstnamelerini çağırmış olduk.
          }


        for(let i in users){
          console.log(`index: ${i} value: ${users[i].lastName}`);
            }

###### map:returns an array


      let veri= users.map(function(item){
        return item.firstName+" "+item.lastName;
          }); console.log(veri);






        let numbers= [1,4,3,5,2];
        let num=numbers.map(function (n) {
            return n*n;
              });
                console.log(num);



****************************************************************************
****************************************************************************
****************************************************************************

## **FONKSİYONLAR**


      function merhaba() {
           console.log("Merhabalar")
              }
                merhaba();





        function x(name,age){
           console.log(`İsim: ${name} Yaş: ${age}`);
            }
            x("Batuhan",29);
            x("alperen",25);
            x("Çiğdem",22);

              function yasHesapla(dogumYili) { 
                return 2022-dogumYili;}

          console.log(yasHesapla(1994));

          let ageBatu= yasHesapla(1994);
            let ageCigdem=yasHesapla(2001);
              console.log(ageBatu);
                console.log(ageCigdem);
 



      function ehliyetAlabilmeDurumu(dogumYili,isim){

        let yas=yasHesapla(dogumYili);
        let ehliyet =18-yas;

          if(ehliyet>0){
           console.log(`${isim} ehliyet alabilmenize ${ehliyet} yıl kaldı`);

          }else{
             console.log(isim+" Ehliyet alabilirsiniz");
         }
       }
          ehliyetAlabilmeDurumu(1994,"Batuhan");
            ehliyetAlabilmeDurumu(2010,"Buse");

***************************************************************************
****************************************************************************
****************************************************************************


## **Window Object**

      veri=window;
        console.log(veri);
        >alert (pop-up açılır)
          alert("Merhabalar");


    >prompt (kullanıcıdan veri almak için)
      var veri2=prompt("Adınızı Giriniz: ");
        console.log("Adınız "+veri2);


        >confirm (Kullanıcıdan evet hayır tarzı onay mesajı istersek)
          veri3= confirm("Çıkmak istediğinize emin misiniz");
            if(veri3){
              console.log("Çıkış gerçekleşti") 
                }else{
                  console.log("Çıkış gerçekleşmedi")}
                    console.log(veri3);


### Location

          veri=window.location.href;
            veri=window.location.hostname;
              veri=window.location.protocol;
                window.location.href="http://batuhanaygun.com";
                  console.log(veri);
