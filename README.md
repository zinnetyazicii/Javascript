# Javascript
### 1. innerHTML()
    - kullanarak bir HTML öğesine yazma.
### 2. Document.write() 
    - kullanarak HTML çıktısına yazma.
### 3. window.alert() 
    - kullanarak bir uyarı kutusuna yazma.
### 4. Console.log() 
    - kullanarak tarayıcı konsoluna yazma.

### Object.
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
      document.getElementById("demo").innerHTML = str.slice(7,13);.
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
### 1. indexOf()
    -  bir dizede belirtilen  metnin  ilk konumunun indeksini döndürür.
    - let str = "Please locate where 'locate' occurs!";
        str.indexOf("locate");
    - Ekran çıktısı : 7 
##### Not: JavaScript, konumları sıfırdan sayar. 0, bir dizedeki ilk konumdur, 1 ikincidir, 2 üçüncüdür, ...
### 2. lastIndexOf()
    - bir dizede belirtilen  metnin  son konumunun indeksini döndürür.
    - let str = "Please locate where 'locate' occurs!";
        str.indexOf("locate");
    - Ekran çıktısı : 21 
#### Uyarı: Her ikisi indexOf()ve lastIndexOf()metin bulunamazsa -1 döndürür:
#### Uyarı: Her iki yöntem de arama için başlangıç ​​konumu olarak ikinci bir parametreyi kabul eder:
    - let str = "Please locate where 'locate' occurs!";
        str.indexOf("locate", 15);
    - Ekran çıktısı : 21 
#### Uyarı: lastIndexOf() sondan başa doğru  arama yapar, yani: ikinci parametre ise , 15arama 15. konumda başlar ve dizenin başına kadar arar.
     - let str = "Please locate where 'locate' occurs!";
        str.indexOf("locate", 15);
    - Ekran çıktısı : 7 

### 3. search()
    -  belirtilen bir değer için bir dize arar ve eşleşmenin konumunu döndürür:
    - let str = "Please locate where 'locate' occurs!";
        str.search("locate");
    - Ekran çıktısı : 7 
#### Fark ettin mi? : indexOf()ve search(), eşit mi? 
    - İki yöntem eşit DEĞİLDİR . Bu farklar:
        + Yöntem search(), ikinci bir başlangıç ​​konumu bağımsız değişkeni alamaz.
        + Yöntem indexOf(), regular expiression (/gi) alamaz. 
### 4. match()
    - bir normal ifadeyle eşleşme için bir dize arar ve eşleşmeleri bir Array nesnesi olarak döndürür.
##### <p id="demo"></p>
    - let text = "The rain in SPAIN stays mainly in the plain"; 
        document.getElementById("demo").innerHTML = text.match(/ain/gi);
    -  Ekran çıktısı : ain,AIN,ain,ain
### 5. includes()
    - dize belirtilen bir değer içeriyorsa, yöntem true değerini döndürür.
    -  let text = "Hello world, welcome to the universe.";
        text.includes("world");
    -  Ekran çıktısı : true
###  string.includes(searchvalue, start)
    - let text = "Hello world, welcome to the universe.";
        text.includes("world", 12);
    -  Ekran çıktısı : false
### 6. startsWith()
    - Bir dize belirtilen bir değerle başlıyorsa true aksi durumda false döndürür
### string.startsWith(searchvalue, start)
    - let text = "Hello world, welcome to the universe.";
        text.startsWith("world", 5)    // Returns false
### 7. endsWith()
    - Bir dize belirtilen bir değerle bitiyorsa true aksi durumda false döndürür
### string.endsWith(searchvalue, length)
    - let text = "Hello world, welcome to the universe.";
        text.endsWith("world", 11); //true
## Template Literals
    - + operataörü kullanmadan  `` içinde yazarak farklı türleri birleştirmeyi sağlar.
    - let firstName = "John";
        let lastName = "Doe";
        let text = `Welcome ${firstName}, ${lastName}!`;
    - let price = 10;
        let VAT = 0.25;
        let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;
    - Ekran çıktısı : Total: 12.50
## Number
### 1. isNaN()
    - Bir değerin sayı olup olmadığını öğrenmek için global JavaScript işlevini kullanabilirsiniz:
    - let x = 100 / "Apple";
        isNaN(x);
    - Ekran çıktısı : true
## Number Methods
### 1. toString()
    - dize olarak bir sayı döndürür.
### 2. toStoExponential()
    - sayı yuvarlatılmış ve üstel gösterim kullanılarak yazılmış bir dize döndürür.
    - bir parametre, ondalık noktanın arkasındaki karakter sayısını tanımlar:
##### <p id="demo"></p>
    - let x = 9.656;
        document.getElementById("demo").innerHTML =
        x.toExponential() + "<br>" + 
        x.toExponential(2) + "<br>" + 
        x.toExponential(4) + "<br>" + 
        x.toExponential(6);
    - Ekran çıktısı :   9.656e+0
                        9.66e+0
                        9.6560e+0
                        9.656000e+0
### 3. toFixed() 
    - belirtilen sayıda ondalık basamakla yazılan sayı ile bir dize döndürür:
##### <p id="demo"></p>
    - let x = 9.656;
        document.getElementById("demo").innerHTML =
        x.toFixed(0) + "<br>" +
        x.toFixed(2) + "<br>" +
        x.toFixed(4) + "<br>" +
        x.toFixed(6);
    - Ekran çıktısı :   10
                        9.66
                        9.6560
                        9.656000
    
### 4. toPrecision()
    - belirtilen uzunlukta yazılmış bir sayı ile bir dize döndürür:
##### <p id="demo"></p>
    - let x = 9.656;
        document.getElementById("demo").innerHTML = 
        x.toPrecision() + "<br>" +
        x.toPrecision(2) + "<br>" +
        x.toPrecision(4) + "<br>" +
        x.toPrecision(6);
    - Ekran çıktısı :   9.656
                        9.7
                        9.656
                        9.65600 
    
### 5. valueOf()
    - sayı olarak bir sayı döndürür.
##### <p id="demo"></p>
    - let x = 123;
        document.getElementById("demo").innerHTML = 
        x.valueOf() + "<br>" +
        (123).valueOf() + "<br>" +
        (100 + 23).valueOf();
    - Ekran çıktısı :   123
                        123
                        123
#### Değişkenleri Sayılara Dönüştürme
### 6. Number()
- Number() Bağımsız değişkeninden dönüştürülen bir sayı döndürür.
- tarihi cast ettiğimizde 1.1.1970'ten bu yana geçen milisaniye sayısını döndürür.
### 7. parseInt()
- Argümanını ayrıştırır ve kayan noktalı bir sayı döndürür
### 8. parseFloat()
- Argümanını ayrıştırır ve bir tamsayı döndürür
#### MAX_VALUE	
- JavaScript'te mümkün olan en büyük sayıyı döndürür
- ```let x = Number.MAX_VALUE;    document.getElementById("demo").innerHTML = x;```
#### MIN_VALUE	
- JavaScript'te mümkün olan en küçük sayıyı döndürür
#### POSITIVE_INFINITY	
- Represents infinity (returned on overflow)
#### NEGATIVE_INFINITY	
- Negatif sonsuzluğu temsil eder (taşma(overflow) durumunda döndürülür)
#### NaN	
- "Sayı Değil" değerini temsil eder

## Array Properties and Methods
### 1. length
Bir lengthdizinin özelliği, bir dizinin uzunluğunu (dizi öğelerinin sayısı) döndürür.
- Son Dizi Öğesine Erişim 
- ```const fruits = ["Banana", "Orange", "Apple", "Mango"];  let fruit = fruits[fruits.length - 1];```
### 2. push()
- Bir diziye yeni bir eleman eklemenin en kolay yolu şu push()yöntemi kullanmaktır:
### 3. toString() 
- JavaScript yöntemi toString(), bir diziyi (virgülle ayrılmış) dizi değerleri dizisine dönüştürür.
### 3. join() 
- Yöntem join()ayrıca tüm dizi öğelerini bir dizgede birleştirir.
- ```const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");```
- Ekran çıktısı : Banana * Orange * Apple * Mango
### 4. pop()
- Yöntem pop(), dizideki son öğeyi kaldırır:
### 5. push()
- Yöntem push(), bir diziye yeni bir öğe ekler (sonda):
### 6. shift()
- Yöntem shift(), ilk dizi öğesini kaldırır ve diğer tüm öğeleri daha düşük bir dizine "kaydırır". (baştan siler ilk baştaki değeri döndürür)
### 7. unshift()
- Yöntem unshift(), bir diziye (başlangıçta) yeni bir öğe ekler ve eski öğeleri "değiştirir":(baştan ekler)
