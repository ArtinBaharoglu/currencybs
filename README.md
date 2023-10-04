

## Exchange Currency Buy/Sell Project

Bu projede döviş alış/satış işlemlerini belirli komisyonlar karşılığında hesaplanması ve TCMB Döviz kurlarının listelemesi sağlanmıştır.

Sırası ile aşağıdaki komutlar çalıştırılmalıdır;

composer update<br>
php artisan key:generate
<br>
php artisan migrate<br>
php artisan serve

TCMB döviz kurları okunurken localde SSL ile ilgili olarak sorun olmaması adına, vendor içerisinde yer alan teknomavi paketi Doviz.php dosyası içerisinde düzenleme yapılmıştır;
<br>
// SSL kontrolünü devre dışı bırakma,
<br>
$curl->setOption(CURLOPT_SSL_VERIFYPEER, false);
<br>
$curl->setOption(CURLOPT_SSL_VERIFYHOST, false);
