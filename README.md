# Java Springboot

## <span style="color: orange;"> Packages </span>

### <span style="color: blue;">- config Package</span>

Swagger gibi third party entegrasyonların kurulduğu yerdir.

### <span style="color: blue;">- controller Package</span>

Ana fonksiyonların kullanıldığı ve çeşitli ihtiyaca göre düzenlendiği kısımdır. Service interfacelerinin, entitylerin request response modellerinin birleştiği yerdir.

### <span style="color: blue;">- service Package</span>

Fonksiyonların ihtiyaçlara göre yazılıp düzenlendiği kısımdır. kendi içerisinde iki package’a ayrılır.

- **<span style="color: blue;">impl (implementation) Package:</span>** Fonksiyonların direkt olarak yazıldığı kısımdır. Detayları bu package içerisinde oluşturulur.
- **<span style="color: blue;">interfaces Package:</span>** impl Package’ı içerisinde oluşturulan fonksiyonların ve işlemlerin bir interface'e aktarılıp proje içerisinde template gibi kullanılmasına olanak tanır. Controller içerisinde bu interfaceleri kullanarak daha rahat ve okunabilir bir kod elde edilir.

### <span style="color: blue;">- exception Package</span>

Proje içerisinde dönebilecek olan hataların belirlenmesi konusunda daha detaylı bilgi sahibi olabilmek için http hata kodlarını customize ettiğimiz package’tır.

### <span style="color: blue;">- entity Package</span>

Proje içerisinde kullanılan entitylerin oluşturulduğu kısımdır. DB tarafında o entitynin nasıl algılanacağı burada belirlenir.

### <span style="color: blue;">- dto Package</span>

Projede kullanılan modellerin oluşturulduğu kısımdır. kendi içerisinde de ikiye ayrılır.

- **<span style="color: blue;">request:</span>** create, put, patch gibi request methodları için oluşturulan modeller buraya eklenirler. Her modelin bu package içerisinde kendi packageları vardır. Örn: request > user > UserRequestDto, userUpdateDto ..
- **<span style="color: blue;">response:</span>** get, getAll gibi fonksiyonlarda kullanılan modellerin bulunduğu package’tır. Her modelin bu package içerisinde kendi packageları vardır. Örn: response > user > UserResponseDto …

### <span style="color: blue;">- repo (repository) Package</span>

Entity interfacelerin oluşturulduğu repository kısmıdır. Veritabanı için o Entity’i tanımlar ve gerekli olan işlemler otomatik olarak sağlanır.
