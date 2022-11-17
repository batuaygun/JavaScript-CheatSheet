#                           **BATUHAN AYGÜN JAVASCRIPT CHEAT SHEET VOL.2**
## ARRAYS

      let names= ["Batuhan","Alperen","Çiğdem","İdil"];
      let years= [1994,1998,2001,1998];
        let mix=["Fenerbahçe","Türkiye",1923,null,undefined,["Yazılım","Futbol","Ülke"]];
          console.log(names);
            console.log(names.length); // Dizinin uzunluğunu gösterir
              console.log(typeof names);
                console.log(years);
                  console.log(mix);

### GET ARRAY ITEM

    console.log(names[3]);   // 0'dan başlar
    
>Çıktısı İdil olur.
### SET ARRAY ITEM

         names[2]="Batu";   // Dizi içindeki değeri değiştirmek için
        console.log(names);


### ADD NEW ITEM IN ARRAY

    names[4]="Arda";
      console.log(names); // dizi içerisindeki eleman sayısını bildiğimiz için böyle yaptık.
 
>dizi içerisindeki eleman sayısını bilmek zorunda değiliz. O zaman bu kodu kullnarak uzunuluğuna ek bir dizi elemanı daha ekler.
    
      names[names.length]="Mehmet";
          console.log(names);

      names.push("Aygün"); // dizinin sonuna eleman ekler. Diğer bir yöntemdir.
          console.log(names);

      names.unshift("Hello"); // Dizinin başına ekler.
          console.log(names);

      names.pop(); // Dizinin son elemanını siler.
          console.log(names);

      names.shift(); // dizinin ilk elemanını siler.
          console.log(names);

      let index=names.indexOf("Alperen");  // Dizinin içindeki elemanın kaçıncı indexte olduğunu belirtir.
          console.log("index:" +index);

      names.reverse(); // Indexler tam terse döner
          console.log(names);

      years.sort();   // Dizide Sıralama yapar. Küçükten büyüğe doğru
          console.log(years);

      names.sort();  // Diziyi alfabetik olarak sıralar.
          console.log(names);

      let veri= names.concat(years); // iki diziyi birleştirmek için kullanılır.
          console.log(veri);

      names.splice(2,0,"ahmet"); // ikinci indexten başlayıp hiçbir indexi silmeden ahmet öğesini diziye ekler
          console.log(names);

      names.splice(2,4,"kemal"); // ikinci indexten başlayıp 4 adet index siler ve yerine belirtilen index atanır. 
          console.log(names);


*****************************************************************************************

### **Koşullar**


#### IF-ELSE


      const firstName= "Batu";
      const userName= "Baygün";
      const age=29;
      const isStudent= true;
      const school="university";

      if(userName=="Baygün"){
        console.log("Merhaba Batu");
          }else{
           console.log("Kullanıcı bulunamadı!!");
            }

      if(age===28){
        console.log("yaşınız: "+age);
          }else{
            console.log("Yaşınız 29 değil" );
                }

      if(isStudent){
        console.log("Hangi bölümde okuyorsun");
          }else{
            console.log("Hangi mesleği yapıyorsunuz");
            }

        if(age>=18){   
 > Bu koşulu uygulamak için yukarıdaki değişkenleri değiştirebiliriz. Örnek olarak yaşı 17 dersek Yaşınız uygun değil sonucu çıkar veya 
   >school olan değşkeni universityden başka bir değer olarak belirlersek eğitim durumun ehliyet almak için yetersiz sonucu çıkar.
        
      if(school=="university"){
          console.log("Ehliyet alabilirsin");
           }else{
             console.log("Eğitim durumun ehliyet almak için yetersiz")
             }
                }else{
                console.log("Yaşınız ehliyet için yetersiz");
                    }

              let id="wew342"
                if(typeof id !="undefined"){
                  console.log("id: "+id);
                    }else{
                     console.log("no id");
                        }




------------------------------------------------------
#### SWITCH 

> Switch Koşul Yapısı 

      let islem=1;
        switch (islem) {
          case 1:
             console.log("1. nolu işlem yapıldı.");
              break;
          case 2:
             console.log("2. nolu işlem yapıldı.");
              break;
          case 3:
             console.log("3. nolu işlem yapıldı.");
              break;
          case 4:
              console.log("4. nolu işlem yapıldı.");
               break;
          default:
              console.log("İşlem yapılmadı");
                }
*****************************************************************************************



      let day;
        switch (new Date().getDay() + 2) {
         case 0:
          day = "pazar";
            break;
          case 1:
           day = "pazartesi";
            break;
          case 2:
           day = "salı";
            break;
          case 3:
           day = "çarşamba";
            break;
          case 4:
           day = "perşembe";
             break;
          case 5:
           day = "cuma";
            break;
          case 6:
           day = "cumartesi";
            break;
            }
              console.log(day);
*****************************************************************************************
              

      const hour = prompt("Saati giriniz");  // Kullanıcıdan saati girmesini de isteyebiliriz.
        switch (true) {
          case (hour >= 6 && hour <= 12):
            console.log("Günaydın");
              break;

          case (hour >= 13 && hour <= 17):
            console.log("İyi günler");
              break;

          case (hour >= 18 && hour <= 24):
            console.log("İyi akşamlar");
              break;
          default:
             console.log("Yanlış zaman");
              }
              
*****************************************************************************************
*****************************************************************************************

### **Object Literals**

    let firstName="Batuhan";
    let lastName="Aygün";

    let firstName2="Batuhan";
    let lastName2="Aygün";   
    
>bu yöntemle oldukça uzun ve yorucu bir kodlama sürecinin içine giriyoruz. 


      let batu=["Batu","Aygün",29,"istanbul"];
      let alp=["alperen","yeşil",24,"bursa"]; 
>Bu yöntemde ise array olarak tanımlayabiliyoruz. Üsttekine göre çok daha kolay ama bu da zor bir işlem.
>Bunların hepsinin yerine object literals kullanarak tek obje içinde tüm bilgileri işleyebiliriz.


      let veri;
        let user={
         userName:"Baygün",
         firstName:"Batuhan",
         lastName:"Aygün",
         age:29,
         hobbies:["spor","kitap","yazılım"],
         address:{
         city:"İstanbul",
         country:"Türkiye",
         phone:"348234239847398274",
          }
      }
        veri=user;
        veri=user.firstName;
        veri=user.lastName;
        veri=user.hobbies;
        veri=user.hobbies.length;
        veri=user.address.city;
        veri=user.address.phone;
    
          console.log(veri);
            console.log(typeof user);

