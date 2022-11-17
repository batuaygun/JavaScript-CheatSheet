# **BATUHAN AYGÜN JAVASCRIPT CHEAT SHEET VOL.4**

## **DOM MANIPULATION**

### Elementlerin Seçilmesi

#### Tek Element Seçimi 

    document.getElementById() metodu

      let veri;
       veri=document.getElementById("header");
        veri=document.getElementById("header").id;
         veri=document.getElementById("header").className;


        veri=document.getElementById("header"); >Kısa kullanım şekli
         veri=veri.id;
          veri=veri.className;

            veri.style.color="red";
              veri.style.fontSize="50px";
                veri.style.fontWeight="bold";
                 veri.style.display="none";

                    document.getElementById("header").innerText="Yapılacaklar"; 
                    document.getElementById("header").innerHTML="<b>ToDo List</b>";




           console.log(veri);
 
              console.log(document.querySelector("#header")); > id seçimi
              console.log(document.querySelector(".card-header")); > class seçimi
              
                console.log(document.querySelector("div")); > div seçimi
                document.querySelector("li").style.color="blue"; > css özelliği değişimi
                
                document.querySelector("li:last-child").style.color="red"; > css özelliği değişimi
                document.querySelector("li:nth-child(2)").style.color="orange"; > renk değişimi

                document.querySelector("li").className="list-group-item list-group-item-danger"; > class name değiştirme
                document.querySelector("li").classList.add("active"); > Class ekleme


**Çoklu Element Seçimi**

        let veri;
        veri=document.getElementsByClassName("list-group-item");
         veri=document.getElementsByClassName("list-group-item")[0];
          veri=document.getElementsByClassName("list-group-item")[2];


        veri=veri[2];
          veri[1].style.fontSize="30px";
            veri[1].style.color="red";
              veri[2].textContent="new item";



        veri=document.getElementsByTagName("li");
          veri=document.getElementsByTagName("a");
    
            veri=document.getElementById("task-list").getElementsByTagName("a");
              veri=document.querySelectorAll("li");
                console.log(veri);


**Elementlerin üzerinde gezinme**


        let value;
          const todoList=document.querySelector(".list-group");
            const todo=document.querySelector(".list-group:nth-child(2)");
              const card=document.querySelector(".card");


          value=todoList;
            value=todo;
              value= card;


 **Child Notes**

        value= todoList.childNodes; > Tüm öğeleri seçer 

        value= todoList.children; > Sadece anlam gereken öğeleri seçer
        value=todoList.children[0]; > 0 olan indexi alır

      value=todoList.children[todoList.children.length-1]; > Var olan listenin son elemanı getirmiş olur.
      value=todoList.children[1].textContent="Değilen Madde"; > 2. madde yani 1. index değişmiş oldu.
      value=card;
      value=card.children;

        value=card.children[1].children[0].textContent="Merhaba"; 
        > cardın içindeki 1. elemana eriştik onun içindeki 0. elemana eriştik ve değiştirdik.
        
        value=todoList.children[0];
        value=todoList.firstElementChild;
        value=todoList.lastElementChild;

        value=todoList.children.length; > uzunluğu görürüz.
        value=todoList.childElementCount; > uzunluğu gösterir.

        value=card;
        value=card.parentElement; > Card'ın parentına gitmiş oluruz.
        value=card.parentElement.parentElement; > card'ın parentının parentına erişmiş oluruz.

        value=todo;
        value= todo.previousElementSibling; > Kardeşler arasında geçişi sağlar Bir öncekine geçmiş olduk.
        value=todo.nextElementSibling; > Kardeşler arasındaki geçiş. Bir sonrakine geçmiş oluruz.

        value=todo.nextElementSibling.nextElementSibling; > iki sonraki kardeşe geçişi sağlamış olur.
    
        value=todo.previousElementSibling.previousElementSibling; > iki önceki kardeşe gideriz. Eğer ki varsa 
        console.log(value);



---------------------------------------------------------------------------------------------------
 **Element Oluşturma** 

      const li=document.createElement("li");

**Add Class**
  
    li.className="list-group-item list-group-item-secondary";
       li.id=""  // bu şekilde de id eklenir.

**Attribute ekleme**

      li.setAttribute("title","new item"); > title ekledik
      li.setAttribute("Data-id","5"); > data-id ekleme
        const text= document.createTextNode("new item"); > text oluşturma
          li.appendChild(text); > oluşturulan texti ekleme


          const a= document.createElement("a");
          a.setAttribute("href","#");
            a.className="delete-item float-right";
              a.innerHTML="<i class='fas fa-times'></i>";


        li.appendChild(a);

            document.querySelector("#task-list").appendChild(li); >Yeni eleman bu şekilde eklendi
              console.log(li);

---------------------------------------------------------------------------------------------------

 **Element Silme**


      const taskList=document.querySelector("#task-list");
      taskList.remove();  // tamamını siler
      taskList.childNodes[7].remove(); // Pek bi useless bu

       taskList.children[3].remove(); // child olarak siler en işlevsel olan bu
       taskList.removeChild(taskList.children[0]); // alternatif silme yöntemi.

**Attribute Silme**

      taskList.children[1].removeAttribute("class");

        for(let i=0;i<taskList.children.length;i++){
         taskList.children[i].removeAttribute("class");
            }
               console.log(taskList);

---------------------------------------------------------------------------------------------------


**Element Güncelleme** 


      const cardHeader=document.querySelector(".card-header");
        const h2=document.createElement("h2");

          h2.setAttribute("class","card-header");
            h2.appendChild(document.createTextNode("Yeni listeler"));
              const parent=document.querySelector(".card");
                parent.replaceChild(h2,cardHeader);



**Class'larda güncelleme**

        const taskList=document.querySelector("#task-list");
          let value;
            link = taskList.children[0].children[0];
              value=link.className;
                value=link.classList;
                  value=link.classList[0];
                    value=link.classList[1];
                      link.classList.add("new");
                        link.classList.remove("new");






 **Attribute güncelleme**

        value=link.getAttribute("href");
          value=link.setAttribute("href","http://batuhanaygun.com");
            value=link.hasAttribute("href"); > attribute sorgulama
              console.log(value);


