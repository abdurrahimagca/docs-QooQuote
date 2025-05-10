# Architecture Decision Record (ADR) - Proje Mimarisinin Belirlenmesi 

## Teknoloji Yığını
Bu projeyi geliştirmek için aşağıdaki teknoloji yığını tercih edilmiştir:
 - [NestJS](https://nestjs.com/)
 - [PostgreSQL](https://www.postgresql.org/)
 - [TypeORM](https://typeorm.io/)
 - [GraphQL](https://graphql.org/)
 - [Flutter](https://flutter.dev/)

### Neden bu teknoloji yığını? 

- **NestJS**: Nest, modüler bir mimari sunduğu için ölçeklenebilir ve bakımı kolaydır. Geniş bir topluluğa ve iyi bir dokümantasyona sahip olması, destek ve kaynak bulmayı kolaylaştırır. GO veya Rust gibi alternatifler olsa da, JavaScript tabanlı bir yığın ekibimiz için daha uygun. Sadece kullanımı daha kolay olduğu için değil, aynı zamanda buluta dağıtımı da oldukça pratik. Express gibi alternatifler de bu avantajları sunabilir, ancak Nest, uygulamaları daha düzenli bir şekilde geliştirmemizi sağlıyor. Ayrıca GraphQL için yerleşik destek sunması, projemiz için büyük bir artı.
- **GraphQL**: GraphQL, API'ler için bir sorgu dili ve bu sorguları çalıştırmak için bir çalışma zamanıdır. REST'e göre daha yavaş çalışsa da, API'lerle etkileşimde daha esnek ve verimli bir yöntem sunar. İstemcilerin yalnızca ihtiyaç duydukları verileri talep etmesine olanak tanır, bu da ağ üzerinden taşınan veri miktarını azaltabilir. Bu özellik, özellikle mobil uygulamalarda, bant genişliğinin sınırlı olduğu durumlarda önemlidir. Ayrıca GraphQL, gerçek zamanlı güncellemeler için yerleşik destek sunar, bu da projemiz için bir avantajdır.
- **PostgreSQL**: Diğer tüm seçimler değiştirilebilir olsa da, PostgreSQL ilişkisel bir veritabanı için en iyi seçenektir. Bunun iki temel nedeni var:
     - JSONB veri türü sunar, bu da sorgulanabilir ve indekslenebilir. Bu özellik, yapılandırılmamış verileri düzenli bir şekilde saklamamıza olanak tanır ve projemiz için oldukça önemlidir.
     - Verileri vektörleştirme ve arama imkanı sağlar. Gelecekte içerik bazlı arama yapmamız gerekebilir ve PostgreSQL bu konuda en iyi seçenektir.
- **TypeORM**: TypeORM, TypeScript ve JavaScript için bir ORM'dir. Piyasada birçok ORM mevcut ve belki de ORM kullanmak her zaman en iyi çözüm değil. Ancak TypeORM, .NET dünyasındaki EntityFramework gibi, veritabanıyla etkileşim kurmanın pratik bir yolunu sunar. Kullanımı kolaydır ve iyi bir dokümantasyona sahiptir. Ayrıca PostgreSQL için yerleşik desteği bulunur, bu da projemiz için bir avantajdır.
***Not:*** Yine de RAW SQL kullanmayı da değerlendirebiliriz.


