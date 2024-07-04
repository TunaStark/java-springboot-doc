# Java Springboot

## Packages

### - config Package

Swagger gibi third party entegrasyonların kurulduğu yerdir.

### - controller Package

Ana fonksiyonların kullanıldığı ve çeşitli ihtiyaca göre düzenlendiği kısımdır. Service interfacelerinin, entitylerin request response modellerinin birleştiği yerdir.

### - service Package

Fonksiyonların ihtiyaçlara göre yazılıp düzenlendiği kısımdır. kendi içerisinde iki package’a ayrılır. 

1. <b>impl (implementation) Package:</b> Fonksiyonların direkt olarak yazıldığı kısımdır. Detayları bu package içerisinde oluşturulur.
2. <b>interfaces Package:</b> impl Package’ı içerisinde oluşturulan fonksiyonların ve işlemlerin bir interface'e aktarılıp proje içerisinde template gibi kullanılmasına olanak tanır. Controller içerisinde bu interfaceleri kullanarak daha rahat ve okunabilir bir kod elde edilir.

### - exception Package

Proje içerisinde dönebilecek olan hataların belirlenmesi konusunda daha detaylı bilgi sahibi olabilmek için http hata kodlarını customize ettiğimiz package’tır.

### - entity Package

Proje içerisinde kullanılan entitylerin oluşturulduğu kısımdır. DB tarafında o entitynin nasıl algılanacağı burada belirlenir.

### - dto Package

Projede kullanılan modellerin oluşturulduğu kısımdır. kendi içerisinde de ikiye ayrılır. 

1. <b>request:</b> create, put, patch gibi request methodları için oluşturulan modeller buraya eklenirler. Her modelin bu package içerisinde kendi packageları vardır. Örn: request > user > UserRequestDto, userUpdateDto ..
2. <b>response:</b> get, getAll gibi fonksiyonlarda kullanılan modellerin bulunduğu package’tır. Her modelin bu package içerisinde kendi packageları vardır. Örn: response > user > UserResponseDto … 

### - repo (repository) Package

Entity interfacelerin oluşturulduğu repository kısmıdır. Veritabanı için o Entity’i tanımlar ve gerekli olan işlemler otomatik olarak sağlanır.
