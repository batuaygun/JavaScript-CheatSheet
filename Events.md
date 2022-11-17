# **BATUHAN AYGÜN JAVASCRIPT CHEAT SHEET VOL.5**
## EVENT LISTENER AND EVENT OBJECT

        const btn= document.querySelector("#btnDeleteAll");

          btn.addEventListener("click",function () { // bu şekilde olablir yada alttaki yöntemle olabilir.
            console.log("butona tıklandı");
              });


         btn.addEventListener("click",btnClick());
           function btnClick() {  
          > Bu şekilde kullanmak hem daha profesyonel bir görünüm sağlar 
          >hem de oluşturulan fonksiyonu istersek başka alanlarda da kullanabiliriz.
          
          console.log("butona tıklandı.");
              }


      const btn2=document.querySelector("#btnAddNewTask");
        btn2.addEventListener("click",btnClick); 
       >burda ise yukarda oluşturduğumuz fonskliyonu başka bir alanda kullandığımızı görüyoruz.
          btn.addEventListener("click",function(a){
   
        let value;
         value=a;
           value=a.target; > nereye tıkladığımızı gösterir
             value=a.target.id; >hangi id ye tıklandığını görürüz.
              value=a.target.classList; > sınıfları listeleriz 
              value=a.type;

   
             a.preventDefault(); 
           > varsayılanı engelle yapısı olarak düşünülebilir. 
           >href ile sayfayı refresh atmayı ya da bir sayfaya yönlendirmeyi kesti gibi algılayabiliriz.
          console.log(value);
            })

---------------------------------------------------------

### MOUSE EVENTS

      const btn=document.querySelector("#btnAddNewTask");
      const ul=document.querySelector("#task-list");

**Click event (tek tık)**

       btn.addEventListener("click",run);
       ul.addEventListener("click",run);


**Double Click  (çift tık)**

                    btn.addEventListener("dblclick",run);

**mouse down event**

            btn.addEventListener("mousedown",run); // mouse bırakana kadar çalışır.

**mouse up event**

          btn.addEventListener("mouseup",run);  // mouse bıraktığın anda çalışır.

**mouse enter**

            ul.addEventListener("mouseenter",run); // mouse üzerine geldiği anda çalışır.


**mouse leave**

          ul.addEventListener("mouseleave",run); // mouse üzerinden ayrıldığı zaman çalışır.

**mouse over**

          ul.addEventListener("mouseover",run); 
          > mouse enter ve mnouse levae ile arasındaki fark alt sınıfına yada butonuna geldiğimizde 
          >mouse over ve mouse out çalışmaya devam eder.

**mouse out**

        ul.addEventListener("mouseout",run);

**mouse move**

          ul.addEventListener("mouseover",run); // hareketimizin piksel cinsinden gösterir kısmen tüm hareketi sayar.

            function run(event){
             console.log(`event type: ${event.type}`);
             }





---------------------------------------------------------
### Keyboard Events
             

            const text= document.getElementById("txtTaskName");

**focus**

            text.addEventListener("focus",run);  // tetiklendiğinde odaklandığını gösterir.

**Blur (onfocus efect)**

              text.addEventListener("blur",run);

**paste** 

          text.addEventListener("paste",run); // dışardan veri getirildiğinde devreye giren event

**copy**
  
          text.addEventListener("copy",run);  // kopyaladığımızda devreye giren event

**cut**

          text.addEventListener("cut",run); // cut işlemi yapıldığında devreye giren event


**select**

          text.addEventListener("select",run); //  sayfa üzerinde bir yapıyı seçtiğimizde devreye giren event


**KeyDown**

          text.addEventListener("keydown",run);  // klavyeden bir tuşa bastığımızda devreye giren event

**Keyup**

          text.addEventListener("keyup",run);  // klavyeden bir tuşa basılıp bırakıldığında devreye girer.


          function run(e){

             console.log(e.type);
             }
