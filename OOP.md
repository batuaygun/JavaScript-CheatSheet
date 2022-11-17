# **BATUHAN AYGÜN JAVASCRIPT CHEAT SHEET VOL.6**

## OOP

### CONSTRUCTOR 

>Obje kavramı= Primitivelerin dışında kalan her şeye obje diyebiliyoruz
>Primitivler= Numbers,String,booleans, Undefined,null

>Oluşturduğumuz objelerin herbir yapıda aynı olmasını isteyebiliriz. Yani
>Her seferinde orda name olsun, job olsun isteyebiliriz.
>Her oluşan nesne bu kalıba bu formata göre oluşsun isteyebiliriz.
>Bu durumda kullanmamız gereken yapı constructor yapısı.
  
      let batu= {
        name:"batu",
          yearOfBirth: 28,
            job:"developer",
            }

      val = batu;
        console.log(val);
          console.timeLog(typeof val);


>Fonksiyon eşliğinde constructor oluşturabiliyoruz


        const tarih= new Date();
  
        function student(name,yearOfBirth,job){
          this.name = name;
            this.yearOfBirth=yearOfBirth;
              this.job=job;
                this.calculateAge=function () {
                  return tarih.getFullYear()-this.yearOfBirth;
                  }
                     console.log(this);
                     }
                     
          let batu = new student("batu", 1994, "mühendis");
          > Constructor yapısı ile yaptığımız için başka bir infoyu kolaylıkla ekleyebiliriz.
            let ali = new student("ali", 1998, "öğrenci");


            console.log(batu.name); // İstediğimiz objedeki bilgiye bu şekilde erişebiliyoruz
              console.log(batu.yearOfBirth);
                console.log(batu.calculateAge());
                  console.log(ali.calculateAge());



>Constructor ı değişken kullanarak da oluşturabiliyoruz. Bu da farklı bir kullanım şekli


          let student = function (name, yearOfBirth, job) {
             this.name = name;
               this.yearOfBirth = yearOfBirth;
                this.job = job;
                  this.calculateAge = function () {
                    return tarih.getFullYear() - this.yearOfBirth;
                    }
                      console.log(this);
                      }

---------------------------------------------------------
---------------------------------------------------------
### **PROTOTYPE**

    
>Miras alma yöntemi (INHERITANCE) 
>Miras alma nedir? == Diyelim ki Person isminde bir objemiz var objenin 
>name, yearOfBirth, job, calculateAge() adından özellikleri olsun.
>Biz bir tane daha obje oluşturduğumuzu varsayalım adı da Teacher olsun
>Teacher özellikleri ise subject ve greeting() olsun,
>ve biz student içindeki ölzellikleri de teacher içinde kullanmak istiyoruz diyelim.
>o zaman student içindeki özellikleri tek tek yazmak yerine student içierisinden miras alıyoruz.
>Miras alma(Inheritance) dediğimiz olay genel hatlarıyla bu şekildedir.

>Javada Class olarak belirrtiğimiz şey hemen hemen aynı yapıda 
>Js içinde Prototype'tır. Örnekte daha kolay anlaşılır. 



          let person= function(name,yearOfBirth,job){
              this.name=name;
                this.yearOfBirth=yearOfBirth;
                this.job=job;}

          let batu=new person("batu",1994,"mühednis");
            let ali=new person("ali", 1998,student);

            person.prototype.calculateAge=function(){
               return 2022-this.yearOfBirth; 
               } 

        person.prototype.getName=function () {
          return this.name;
          }

      console.log(batu.calculateAge());
        console.log(batu);
          console.log(batu.getName());

          console.log("**************")
            console.log(ali.getName());
              console.log(ali)
                  console.log(ali.calculateAge());


---------------------------------------------------------
---------------------------------------------------------
### **Object-Create**

**Object.create**

>Var olan bir objenin özelliğini yeni oluşturacağımız bir nesnenin içerisine prototype şeklinde ekleme yöntemidir.

    
        let personProto= {
            calculateAge:function () {
            return 2022-this.yearOfBirth;
             }
          }

        let batu= Object.create(personProto);

            batu.name="batu";
              batu.yearOfBirth=1994;
                batu.job="student";


            let ali=Object.create(personProto,{
               name:{value:"ali"},
                  yearOfBirth:{value:1998},
                    job:{value:"teacher"},
                     });
                     
                      console.log(batu);
                        console.log(batu.calculateAge());

                      console.log(ali);
                         console.log(ali.calculateAge());

---------------------------------------------------------
---------------------------------------------------------

### **IMMEDIATE FUNCTIONS**


>Bir fonksiyonun sadece bir kez çalışmasını istiyorsak kullanacağımız yöntem budur.
>Örnek olarak bir kullanıcının siteye girdikten sonra karşılacağı welcome fonksiyonu sadece bir kez çalışsın demek gibi.


>Burası normal fonksiyon 

          function welcome() {
        var days=["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
          var today =new Date();
            var msg="Hoşgeldiniz. Bugün  "+days[today.getDay()];
              return msg;
              }
              console.log(welcome()); 

  >Immediate için iki yöntem var 
  1.
    
            (function(){
           }());

2.

            (function(){
           })();

--------------------------------------
          (function(){

             var days=["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
                var today =new Date();
                   var msg="Hoşgeldiniz. Bugün  "+days[today.getDay()];
                    console.log(msg);
                    }());

>içerideki paranteze value ekleyebiliriz mesela

          (function(name){

              var days=["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
                var today =new Date();
                  var msg="Hoşgeldiniz " +name+  ' Bugün '+days[today.getDay()];
                    console.log(msg);
                    }("Batu"));


