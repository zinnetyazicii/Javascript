# Javascript
### 1. innerHTML() 
    - kullanarak bir HTML öğesine yazma.
### 2. Document.write() 
    - kullanarak HTML çıktısına yazma.
### 3. window.alert() 
    - kullanarak bir uyarı kutusuna yazma.
### 4. Console.log() 
    - kullanarak tarayıcı konsoluna yazma.

### Object
    - const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};

## HTML Events
### 1. onchange()
    - Bir HTML öğesi değiştirildi
### 2. onclick()	
    - Kullanıcı bir HTML öğesini tıkladığında
### 3. onmouseover()
    - Kullanıcı, fareyi bir HTML öğesinin üzerine getirir
### 4. onmouseout()	
    - Kullanıcı, fareyi bir HTML öğesinden uzaklaştırır
### 5. onkeydown()	
    - Kullanıcı bir klavye tuşuna basar
### 6. onload()	
    - Tarayıcı sayfayı yüklemeyi tamamladı

##    String Methods
### 1. length 
    - bir dizenin uzunluğunu döndürür.
### 2. slice(start, end)
    - bir dizgenin bir bölümünü çıkarır ve çıkarılan bölümü yeni bir dizgede döndürür.
    - Yöntem 2 parametre alır: başlangıç ​​konumu ve bitiş konumu (bitiş dahil değildir).

    ```
    let str = "Apple, Banana, Kiwi";        
    document.getElementById("demo").innerHTML = str.slice(7,13);    
    ```
    - Ekran çıktısı : Banana
### 3. substring(start, end)
### 4. substr(start, length)
