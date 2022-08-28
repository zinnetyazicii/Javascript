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
    - let str = "Apple, Banana, Kiwi";        
      document.getElementById("demo").innerHTML = str.slice(7,13);
    - Ekran çıktısı : Banana
##### Not: JavaScript, konumları sıfırdan sayar.İlk konum 0'dır.İkinci konum 1'dir.Bir parametre negatifse, konum dizenin sonundan sayılır.
    - let str = "Apple, Banana, Kiwi";
      let part = str.slice(-12, -6);
    - Ekran çıktısı : Banana
##### Not: İkinci parametreyi atlarsanız, yöntem dizenin geri kalanını dilimler halinde kesecektir
    - let str = "Apple, Banana, Kiwi";
      document.getElementById("demo").innerHTML = str.slice(7);
    - Ekran çıktısı : Banana, Kiwi
    - let str = "Apple, Banana, Kiwi";
        document.getElementById("demo").innerHTML = str.slice(-12
    - Ekran çıktısı : Banana, Kiwi
### 3. substring(start, end)
    - slice() ile benzerdir.
    - Aradaki fark, 0'dan küçük başlangıç ​​ve bitiş değerlerinin
    - let str = "Apple, Banana, Kiwi";
      document.getElementById("demo").innerHTML = str.substring(7,13);
    - Ekran çıktısı : Banana
##### Not: İkinci parametreyi atlarsanız, substring() dizenin geri kalanını kesecektir.

### 4. substr(start, length)
    - slice() ile benzerdir.
    - Fark, ikinci parametrenin çıkarılan parçanın uzunluğunu belirtmesidir.
    - let str = "Apple, Banana, Kiwi";
      document.getElementById("demo").innerHTML = str.substr(7,6);
    - Ekran çıktısı : Banana
##### Not: İkinci parametreyi atlarsanız, substr()dizenin geri kalanını kesecektir.
##### Not: İlk parametre negatifse, konum dizenin sonundan itibaren sayılır.
    - let str = "Apple, Banana, Kiwi";
      document.getElementById("demo").innerHTML = str.substr(-4);
    - Ekran çıktısı : Kiwi
### 5. replace()
    -  belirtilen bir değeri bir dizedeki başka bir değerle değiştirir:
    - Yöntem yalnızca ilk eşleşmenin yerini alır.
    - replace()yöntem büyük/küçük harf duyarlıdır.
##### <p id="demo">Please visit Microsoft and Microsoft!</p>
    - function myFunction() {
        let text = document.getElementById("demo").innerHTML; 
        document.getElementById("demo").innerHTML =
        text.replace("Microsoft","W3Schools");
        }
    - Ekran çıktısı : Please visit Microsoft and Microsoft!
    - Büyük/küçük harf duyarlılığını değiştirmek için,regular expression bayrağı kullanın: /i
##### Not: Normal ifadeler tırnak işaretleri olmadan yazılır.
##### <p id="demo">Please visit Microsoft!</p>
    - function myFunction() {
        let text = document.getElementById("demo").innerHTML; 
        document.getElementById("demo").innerHTML =
        text.replace(/MICROSOFT/i,"W3Schools");
        }
    -  Ekran çıktısı : Please visit Microsoft and Microsoft!
    - Tüm eşleşmeleri değiştirmek için regular expression  ( genel eşleşme) bayrağı kullanın :/g
##### <p id="demo">Please visit Microsoft and Microsoft!</p>
    - function myFunction() {
        let text = document.getElementById("demo").innerHTML; 
        document.getElementById("demo").innerHTML =
        text.replace(/Microsoft/g,"W3Schools");
        }
    - Ekran çıktısı : Please visit Microsoft and Microsoft!
### 6. toUpperCase()
    - Bir dize şu şekilde büyük harfe dönüştürülür 
    - let text1 = "Hello World!";
      let text2 = text1.toUpperCase();
### 7. toLowerCase()
    - Bir dize, şu şekilde küçük harfe dönüştürülür 
### 8. concat()
    - iki veya daha fazla dizeyi birleştirir.
    - let text1 = "Hello";
        let text2 = "World";
        let text3 = text1.concat(" ", text2);
    - concat(), artı operatörü yerine kullanılabilir. Bu iki satır aynı şeyi yapar:
    - text = "Hello" + " " + "World!";
        text = "Hello".concat(" ", "World!");
### 9. trim()
    - bir dizgenin her iki tarafındaki boşlukları kaldırır:
    - let text1 = "      Hello World!      ";
      let text2 = text1.trim();
### 10. trimStart()
    - trim() gibi çalışır ancak boşlukları yalnızca bir dizenin başlangıcından kaldırır.
### 11. trimEnd()
    - trim() gibi çalışır ancak boşlukları yalnızca bir dizenin sonundan kaldırır.
### 12. padStart()
    - bir dizeyi başka bir dizeyle doldurur:
##### <p id="demo"></p>
    - let text = "5";
    document.getElementById("demo").innerHTML = text.padStart(4,"x");
    - Ekran çıktısı : xxx5
### 13. padEnd()
    - bir dizeyi başka bir dizeyle doldurur:
##### <p id="demo"></p>
    - let text = "5";
      document.getElementById("demo").innerHTML = text.padStart(4,"0");
    - Ekran çıktısı : 0005
##### Not: Yöntem padEnd()bir dize yöntemidir.Bir sayıyı doldurmak için önce sayıyı bir stringe dönüştürün.
    - let numb = 5;
        let text = numb.toString();
        let padded = text.padEnd(4,"0");
### 14. charAt(position)
    - bir dizgede belirtilen bir dizindeki (konumdaki) karakteri döndürür:
    - let text = "HELLO WORLD";
        let char = text.charAt(0);
### 15. charCodeAt(position)
    - bir dizgede belirtilen bir dizindeki karakterin unicode'unu döndürür:
    - Yöntem bir UTF-16 kodu (0 ile 65535 arasında bir tam sayı) döndürür.
### 16. Property access [ ]
    - [ ] dizelerde özelliğine erişime izin verir:
    - let text = "HELLO WORLD";
        let char = text[0];
### 17. split()
    - şu yöntemle bir diziye parçalanabilir
##### <p id="demo"></p>
    - let text = "a,b,c,d,e,f";
        const myArray = text.split(",");
        document.getElementById("demo").innerHTML = myArray[0];
    - Ekran çıktısı : a
    - parametre  atlanırsa, döndürülen dizi tüm dizeyi [0] dizininde içerecektir.
    - Ayırıcı "" ise, döndürülen dizi tek karakterlik bir dizi olacaktır:
## String Search