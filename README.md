# form_manager
formdan gelen melumatlari yoxlmaq ucun

   KLAS HAQQINDA MELUMAT VE ISLETME NUMUNELERI
    
    Class bezi metinlerde gormek istemediyiniz sozleri istediyiniz sozle evez etmek ucun
    elverisli metodlara malikdir. Bundan elave siz xaricden oz ifadelerinizi ve onlari
    evez eden sozleri elave ede bilersiniz . Daxili ifade evezleyicileri istifade etmek is-
    teyirsinizse:
        
        obyekt=form_manager('sizin metn') yazmaqiniz kifayet edir
    Bundan basqa siz xaricden ifade ve evezini de daxil ede bilersiniz....................
    Oz ifadelerinizi daxil etmek ucun siz konstruktor icerisine develop=True acarini daxil
    etmelisiniz byekt=replacer(metn,luqet,develop=True) luqetin dictionary formatinda  
    olmasi sertdir...
    Numune:
        
         metn='en gozel cihaz n1-dir
         luqet = {'en gozel cihaz':'asus'} / cumle tapa bilmedim :)
         obyekt=form_manager(metn,luqet,develop=True) 
         obyekt.translate()
         
         cixis:
             
             asus n1-dir
             
    Yuxaridaki numunede sadece cumlede belli metin evezlenecek eyer ifadenin kecdiyi her bir yeri evezle-
    mek isteyirsinizse translate(any=True) seklinde yazmalisiniz
    Numune:
         metn='en gozel cihaz n1-dir
         luqet = {'en gozel cihaz':'asus'} / cumle tapa bilmedim :)
         obyekt=form_manager(metn,luqet,develop=True) 
         obyekt.translate() //
         bu numuneni deyisdirib metn='en gozel cihaz n1-dirler' yazsaq islemeyecek bunun ucun bucur yazilmalidir
         Numune:
         metn='en gozel cihaz n1-dir' / sonra istenilen xarakter ola biler
         luqet = {'en gozel cihaz':'asus'} / cumle tapa bilmedim :)
         obyekt=form_manager(metn,luqet,develop=True) 
         obyekt.translate(any=True)
        
    Yuxaridaki numunede translate metodu icerisine up=True acarini daxil etseniz cumlenin
    ilk herfi boyudulecek  ve  noqteden sonraya bosluq elave edilecek ve noqteden sonraki ilk herf boyu-
    dulecek...
    Numune:
        
        obyekt.translate(up=True)
        
    Hemcinin klasda metinde tekrar olunan soz ve on-
    larin sayini gosteren, cumlenin uzunluq hecmi, xarakterlerin tekrar sayi, bosluq
    kimi atrribular movcuddur.
    
    Numune:
        obyekt.uzunluq / cumlenin xarakter sayi
        obyekt.bosluq /  cumledeki sozler arasi bosluq sayi
        obyekt.sozlerin_tekrar_sayi / cumledeki her soz ve onlarin cumlede islenme sayi (dictionary formatinda)
        obyekt.tekrar_xarakter_sayi / cumledeki her bir xarakter ve onun tekrar sayi (dictionary formatinda)
    
    _____________________________Konstruktor olmadan da isleyecek metodlar______________________________
    Bundan basqa siz form_manager klasinin konstruktorunu bos qoyaraq da nomre yoxlama kimi metodddan istifade 
    ede bilersiniz
    Numune:
        opyekt=form_manager()
        obyekt.nomer('sizin nomre') // bu formatda meselen 0555555555
        Nomer metodu size nomrein standarta uyqun olub olmadiqini bildiren deyer True yaxud False qaytarir
        Siz metoddan istifade etdikden sonra onun operator ve format atributlarini ala bilersiniz
        Numune:
            opyekt=form_manager()
            obyekt.nomer('sizin nomre') // bu formatda meselen 0555555555
            obyekt.format // nomrenin formati meselen 055
            obyekt.operator // nomrenin operatoru meselen Bakcell
            
            
     Mail metodu daxil olan formatinin duzgun olub olmadiqini gosterir ve gmail mail servislerini destekleyir
     Numune:
         
         obyekt.mail('asus_09@gmail.com') / True qaytaracaq
         obyekt.mail('asus_09@mail.ru') / True qaytaracaq
         Xatirladim ki mailde reqem ve altdan xett (_)-e icaze verilir normal mailde olduqu kimi
         
    Sayt metodu duzgun sayt girmeye xidmet edir:
        Numune:
            
            obyekt.sayt('sayt.az') // True qaytaracaq
            xatirladim ki sayt adi minimum uc maksimum 10, domen adi is minimum 2 maksimum 5 herfli ola biler
            sayt adinda reqemlere icaze verilir
            obyekt.sayt('sensiz52.com') // True qaytaracaq
         
         
    
    SOKUN OYRENIN PAYLASIN ILK VERSIYA HERAKL TEREFINDEN YAZILIB   
