Word belgesinde makro yazabilmek için öncelikle ayarlar kısmına gelip "Şeridi özelleştir'e" tıkladıktan sonra sağ tarafta "Geliştir" seçeneğini aktif etmeniz gerekmektedir. 
![0](https://github.com/meisterlos/Word_Makro/assets/81145753/84861d84-efe3-416d-97b0-9c0f9f4cc42a)

Daha sonrasında saldırı makinemize geliyoruz ve veil aracını kurduktan sonra veil aracımızı çalıştırıp "use 1" komutunu kullanalım.
![1 1](https://github.com/meisterlos/Word_Makro/assets/81145753/10e17558-8f29-430a-8ce5-b70373c5d589)
Daha sonrasında "list" komutunu kullanarak içerisindeki modülleri listeliyoruz ve ben bu örneğimde "use 21" komutunu kullanıp powershell/meterpreter/rev_https.py modülünü seçiyorum. Burada rev_tcp veya rev_http de seçebilirsiniz tercih sizin.
![2](https://github.com/meisterlos/Word_Makro/assets/81145753/99350c6d-c460-4386-b20a-23ef70c48e4a)

Daha sonrasında kendi ip adresimizi ve istediğimiz bir port numarasını giriyoruz. Burada girdiğiniz port numarası hem karşı cihazda kullanılmayıp hemde ortamdaki firewall tarafından izin verilmiş bir port olması lazım! Dosyayı istediğiniz isim ile kaydedin.
![3 3](https://github.com/meisterlos/Word_Makro/assets/81145753/97067570-cd3d-4790-bb6d-518c767c9d5c)
Program bize bir adet .bat uzantılı bir dosya oluşturdu şimdi bu bat dosyasını direkt karşı cihaza atar isek antivirüs tarafından engellenecektir. Bunun için veil programında bulunan bir başka modülü daha kullanacağız.
Veil programında "use 3" komutunu kullanın ve auxuliary/macro_converter modülünü seçelim.
![4](https://github.com/meisterlos/Word_Makro/assets/81145753/05d646ea-dbc4-4711-befb-24ccc83b55d6)
Bu kısımda oluşturduğumuz .bat uzantılı dosyayı kullanacağız ve set POSH_BATCH dosya_yolu.bat diye komutumuzu yazalım.
![5](https://github.com/meisterlos/Word_Makro/assets/81145753/594fb3fa-65e6-4162-8e79-03e31b35b88f)
Program şimdi bize bir adet .txt uzantılı dosya verdi Bu vermiş olduğu dosyayı açıp içerisindeki kodu kopyalayın ve word dosyanıza gelin. Word'de bulunan geliştir
sekmesine tıkladıktan sonra makro oluşturup içerisine bu komutu yapıştıralım. Ardından word dosyamızda makroları çalıştırabilmek için dosya uzantısını değiştirmek gerekiyor. Farklı kaydete tıklayın ve .docm .doc veya .dotm dosya uzantısında kaydedin.
![8](https://github.com/meisterlos/Word_Makro/assets/81145753/15cc582c-4b12-40fe-9f78-628bb83e13ae)
Saldırı makinemizde veil programı bize .rc uzantılı bir dosya'da vermişti eğer isterseniz direkt olarak aşağıdaki komuttaki gibi kullanıp dinlemeye alabilirsiniz. Veil'in oluşturduğu .rc uzantısı metasploitteki exploit/multi/hundler'ı çalıştırır ve otomatik şekilde sizin vermiş olduğunuz ip adresini ve portu dinlemeye alır.
![6](https://github.com/meisterlos/Word_Makro/assets/81145753/d35bc334-5916-4003-a1b1-695797fb691e)

Eğer isterseniz netcat aracını'da kullanabilirsiniz, benim tavsiyem metasploit freamworkü kullanmak.
Hedef kişi word dosyasını açtıktan sonra shell almış olacaksınız.
![7](https://github.com/meisterlos/Word_Makro/assets/81145753/b9dc2470-f0e8-4d56-bd81-845e0594d768)
